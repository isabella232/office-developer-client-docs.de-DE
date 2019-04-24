---
title: Formular Konfigurationsdatei [Beschreibung] Abschnitt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320986"
---
# <a name="form-configuration-file-description-section"></a>Formular Konfigurationsdatei [Beschreibung] Abschnitt
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Description]** enthält alle Eigenschaften des Formulars, die Steuerelementen in der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die beim Auffinden des Formulars verwendet werden. Die **MessageClass**-, **CLSID**-und **Display** Name-Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. . Die restlichen Einträge sind optional. Das Format des Abschnitts **[Description]** lautet: 
  
Der Abschnitt **[Description]** enthält alle Eigenschaften des Formulars, die Steuerelementen in der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die beim Auffinden des Formulars verwendet werden. Die **MessageClass**-, **CLSID**-und **Display** Name-Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. . Die restlichen Einträge sind optional. Das Format des Abschnitts **[Description]** lautet: 
  
 **Beschreibung MessageClass** =  -_Zeichenfolge_
  
 **CLSID** =  -_GUID_
  
 **** =  _Anzeige_ Name
  
 **SmallIcon** =  -_Pfad_
  
 **LargeIcon** =  -_Pfad_
  
Optionale Einträge sind:
  
 **Kategorie** =  _angezeigte Zeichenfolge_
  
 **Unterkategorie** =  _angezeigte Zeichenfolge_
  
 **Kommentar** =  _angezeigte Zeichenfolge_
  
 **** =  _Angezeigte Zeichenfolge_ des Besitzers
  
 **** Angezeigte Zeichen_Folge_  =  
  
 **** =  _Ganze Zahl_
  
 **Gebietsschema** =  -_Zeichenfolge_
  
 **Ausgeblendete** =  _Ganzzahl_
  
 **DesignerToolName** =  -_Zeichenfolge_
  
 **DesignerToolGuid** =  -_CLSID_
  
 **DesignerRuntimeGuid** =  -_CLSID_
  
 **ComposeInFolder** =  _0 | 1_
  
 **ComposeCommand** =  -_Zeichenfolge_
  
Die Einträge **Category** und SubCategory werden von Formular Installationsprogrammen verwendet, um die Standard Kategorisierung von Formularen in der Benutzeroberfläche der Clientanwendung einzurichten. **** Beispielsweise könnte eine Hierarchie eingerichtet werden, in der "Help Desk" die Kategorie und "Software" und "Hardware" waren die Unterkategorien. Diese Kategorisierung kann dann von Viewer-Anwendungen verwendet werden, um Nachrichten auf eine strukturiertere Weise anzuzeigen. Die Einträge **Kommentar**, **Besitzer**und **Anzahl** sind alle Kommentarzeichenfolgen, die auf der Benutzeroberfläche der Clientanwendung angezeigt werden. Hierbei handelt es sich um formularspezifische Eigenschaften, die nach Ermessen des Formular Entwicklers verwendet werden können. Der **Kommentar** Eintrag kann beispielsweise verwendet werden, um den Zweck des Formulars anzugeben, den **Besitzer** Eintrag, der die Person oder Organisation angibt, die für die Verwaltung des Formulars zuständig ist, und die Nummer, die zum Nachverfolgen der verschiedenen Formularversionen verwendet wird. Für den **Kommentar** Eintrag können bis zu zehn Zeilen mit Kommentaren enthalten sein. Die erste Codezeile verwendet das Wort "comment" als Schlüssel, in der zweiten Kommentar Reihe wird "Comment1" als Schlüssel verwendet, und so weiter über "Comment9". 
  
Die **LargeIcon** -und **SmallIcon** -Einträge werden verwendet, um den Pfad für die Symbolressourcen anzugeben, die zum Anzeigen der Symbole in der Benutzeroberfläche der Clientanwendung verwendet werden, in der Regel für Tabellenzeilen, die das **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaftsspalten. Symboldateinamen können als Pfadnamen relativ zu dem Verzeichnis angegeben werden, in dem die Formular Konfigurationsdatei installiert ist. Der **Versions** Eintrag wird verwendet, um die Versionsnummer des Formulars anzugeben. **Locale** ist der Sprachenbezeichner aus drei Buchstaben der Zielformular Bibliothek. Eine Liste dieser Bezeichner finden Sie unter _Win32 Programmer es Reference_.
  
Der **Ausgeblendete** Eintrag gibt an, ob das Formular in der Benutzeroberfläche eines Formularbibliothek Anbieters angezeigt werden soll: 1 gibt an, dass die Datei ausgeblendet ist, und 0 gibt an, dass das Formular sichtbar ist. Nachfolgend sehen Sie eine Beispiel-Formular Konfigurationsdatei. 
  
Der **ComposeInFolder** -Eintrag steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers abgelegt werden soll, wenn der Benutzer die Nachricht beim Erstellen speichert: 1 gibt an, dass das Formular in den aktuellen Ordner verschoben werden soll, und 0 gibt an, dass es Wechseln Sie in den Posteingang. 
  
Der **ComposeCommand** -Eintrag ist die Zeichenfolge, die im Verfassen-Menü der Clientanwendung angezeigt werden soll. Wenn dies nicht angegeben wird, wird der Eintrag **DisplayName** verwendet. 
  
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


