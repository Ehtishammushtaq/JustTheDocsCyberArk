---
title: Scripts
layout: home
nav_order: 10
---

> Script for Activity

```batch

Add-Type @"
using System;
using System.Runtime.InteropServices;
public class User32 {
    [DllImport("user32.dll", CharSet = CharSet.Auto, SetLastError = true)]
    public static extern IntPtr GetForegroundWindow();
    
    [DllImport("user32.dll", CharSet = CharSet.Auto, SetLastError = true)]
    public static extern int GetWindowText(IntPtr hWnd, System.Text.StringBuilder text, int count);
}
"@

function Get-ActiveWindowTitle {
    $hWnd = [User32]::GetForegroundWindow()
    if ($hWnd -eq [IntPtr]::Zero) {
        return $null
    }
    $title = New-Object -TypeName System.Text.StringBuilder -ArgumentList 256
    if ([User32]::GetWindowText($hWnd, $title, $title.Capacity) -gt 0) {
        return $title.ToString()
    }
    return $null
}

$TextToType = "Simplicity is the ultimate sophistication"

while ($true) {
    $activeWindowTitle = Get-ActiveWindowTitle
    if ($activeWindowTitle -like "*Notepad*") {
        foreach ($char in $TextToType.ToCharArray()) {
            Add-Type -AssemblyName System.Windows.Forms
            [System.Windows.Forms.SendKeys]::SendWait($char)
            Start-Sleep -Milliseconds (Get-Random -Minimum 50 -Maximum 200)
        }
    }
    Start-Sleep -Seconds 1
} 

```

> Script for page refresh

```batch

Add-Type -AssemblyName
    'System.Windows.Forms'

While($true) {
    [System.Windows.Forms.Sendkeys]::SendWait('^r')
    Start-Sleep -Seconds 1
}

```