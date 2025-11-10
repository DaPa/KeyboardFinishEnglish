The keyboard layout file has two parts:
- the key mapping and
- the locale name.

By keeping the Finnish key mapping but setting the locale to English, one gets Finnish key positions but Windows will show "Shift" instead of "Vaihto".


# Steps to Create a Finnish Layout with English Labels using MSKLC
## 1. Install MSKLC
Install "Microsoft Keyboard Layout Creator" [MSKLC 1.4](tool/install%20kit/MSKLC.msi). Works fine on Windows 10.

## 2. Load Finnish Layout
Open MSKLC. From the top menu: File → Load Existing Keyboard… Choose Finnish from the list: the Finnish layout should be displayed.

## 3. Save as a New Layout
Go to Project → Properties. Change the following:
- Name: e.g. Finnish-English
- Description: something like Finnish keys, English language for modifiers.
- Language: English (United States) or English (United Kingdom).
        ⚠️ This is the key step — it forces Windows to show English modifier names like Shift.
- Save the project.

## 4. Build the Layout
Click Project → Build DLL and Setup Package.
Choose a folder where the output will be placed: MSKLC will generate an installer [FinEng_amd64.msi](FinEng/FinEng_amd64.msi).

## 5. Install and Select It
Go to the output folder.
Run setup.exe to install the new layout.
Open Settings → Time & Language → Language → Keyboard.
Add the new custom layout under English (US/UK) — or set it directly as the default keyboard.

## 6. Switch and Test
Use Win + Space to switch layouts.
Open Word, Notepad, or Explorer → hover over shortcut hints.
It should show Shift, Ctrl, Alt in English, even though the keys behave like Finnish.

# 👉 Result:

Physical keys = Finnish placement (ö, ä, etc.).

Shortcut labels in Windows = English (e.g. "Shift+Ctrl+S").

