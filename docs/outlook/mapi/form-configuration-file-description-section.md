---
title: Formular Konfigurationsabschnitt Datei [Beschreibung]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d3673c3b10afb55121339e335163ce9b2e5937e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791709"
---
# <a name="form-configuration-file-description-section"></a>Formular Konfigurationsabschnitt Datei [Beschreibung]
 
**Betrifft**: Outlook 
  
Im Abschnitt **[Beschreibung]** enthält alle Eigenschaften des Formulars, die Steuerelemente in des Formulars die Benutzeroberfläche und Attribute, die verwendet werden, bei der Suche nach dem Formular zugeordnet sind. Die **MessageClass**, **Clsid**und **DisplayName** -Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und die Nachrichtenklasse Anzeigename, jeweils zu identifizieren, sind erforderliche Einträge verwendet, um das Formular in der Formularbibliothek gesucht werden soll. . Die verbleibenden Einträge sind optional. Das Format des Abschnitts **[Beschreibung]** lautet: 
  
Im Abschnitt **[Beschreibung]** enthält alle Eigenschaften des Formulars, die Steuerelemente in des Formulars die Benutzeroberfläche und Attribute, die verwendet werden, bei der Suche nach dem Formular zugeordnet sind. Die **MessageClass**, **Clsid**und **DisplayName** -Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und die Nachrichtenklasse Anzeigename, jeweils zu identifizieren, sind erforderliche Einträge verwendet, um das Formular in der Formularbibliothek gesucht werden soll. . Die verbleibenden Einträge sind optional. Das Format des Abschnitts **[Beschreibung]** lautet: 
  
 **[Beschreibung] MessageClass** =  _Zeichenfolge_
  
 **CLSID** =  _Guid_
  
 **DisplayName** =  _Displayedstring_
  
 **SmallIcon** =  _Pfad_
  
 **LargeIcon** =  _Pfad_
  
Optionale Einträge sind:
  
 **Kategorie** =  _Zeichenfolge angezeigt_
  
 **Unterkategorie** =  _Zeichenfolge angezeigt_
  
 **Kommentar** =  _Zeichenfolge angezeigt_
  
 **Besitzer** =  _Zeichenfolge angezeigt_
  
 **Anzahl** =  _Zeichenfolge angezeigt_
  
 **Version** =  _ganze Zahl_
  
 **Gebietsschema** =  _Zeichenfolge_
  
 **Ausgeblendete** =  _ganze Zahl_
  
 **DesignerToolName** =  _Zeichenfolge_
  
 **DesignerToolGuid** =  _Clsid_
  
 **DesignerRuntimeGuid** =  _Clsid_
  
 **ComposeInFolder** =  _0 | 1_
  
 **ComposeCommand** =  _Zeichenfolge_
  
Die **Kategorie** und eine **Unterkategorie** Einträge werden vom Formular Installer zum Einrichten der standardmäßigen Kategorisierung von Formularen in die Benutzeroberfläche für Client-Anwendung verwendet. Beispiel eine Hierarchie konnte eingerichtet werden, auf dem "Help Desk" für die Kategorie ist und "Software" und "Hardware" wurden die Unterkategorien aus. Diese Kategorisierung kann dann von Clientanwendungen Viewer zum Anzeigen von Nachrichten in übersichtlicher Weise verwendet werden. Die **Kommentar**, **Besitzer**und die **Anzahl** der Einträge sind alle Kommentarzeichenfolgen, die in der Benutzeroberfläche der Anwendung angezeigt werden. Dies sind bestimmte Formulareigenschaften im Ermessen des Entwicklers Formular verwendet werden können. Beispielsweise kann der Eintrag **Kommentar** an den Zweck des Formulars, den **Besitzer** Eintrag verwendet, um die Person oder Organisation verantwortlich für die Verwaltung des Formulars anzuzeigen und die Anzahl verwendet, um eine andere Version des Formulars Nachverfolgen verwendet werden. Für den **Kommentar** kann bis zu 10 Textzeilen Kommentare-Eintrag eingefügt werden. Die erste Zeile des Kommentare wird das Wort "Comment" als Schlüssel verwendet, die zweite Zeile von Kommentaren verwendet "Comment1" als Schlüssel, und so weiter bis "Comment9." 
  
Die Einträge **LargeIcon** und **SmallIcon** dienen zum Angeben des Pfads für die Symbolressourcen verwendet, um die Symbole in der Clientanwendung-Benutzeroberfläche angezeigt, in der Regel ist dies für die Zeilen, in denen die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder Spalten für **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). Symbol Dateinamen können als Pfadnamen relativ zu dem Verzeichnis angegeben werden, in die Konfigurationsdatei Formular installiert ist. Der Eintrag **Version** wird verwendet, um die Versionsnummer des Formulars anzugeben. **Gebietsschema** ist die drei Buchstaben bestehende Sprach-ID der Formularbibliothek Ziel. Eine Liste dieser Bezeichner finden Sie in der _Win32 Programmer's Reference_.
  
Der **Hidden** -Eintrag gibt an, ob das Formular in ein Formular Bibliotheksanbieter-Benutzeroberfläche angezeigt werden sollen: 1 bedeutet, dass die Datei ist ausgeblendet, und 0 bedeutet, dass das Formular sichtbar ist. Eine Beispielkonfigurationsdatei Formular wird nach angezeigt. 
  
Der Eintrag **ComposeInFolder** steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers platziert werden, wenn der Benutzer die Nachricht beim Verfassen sie speichert entwickelt wurde: 1 bedeutet, dass das Formular im aktuellen Ordner sollten und 0 bedeutet, dass es sollten Wechseln Sie im Posteingang. 
  
Der **ComposeCommand** -Eintrag ist die Zeichenfolge, die in der Clientanwendung platziert werden die im Menü verfassen. Wenn dies nicht angegeben wird, wird der Eintrag **"DisplayName"** verwendet werden. 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


