---
title: Abschnitt "Form Configuration File [Description]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a55dc1f7c773e79682df8a7fa2ed43d133dd9dbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630873"
---
# <a name="form-configuration-file-description-section"></a>Abschnitt "Form Configuration File [Description]
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Beschreibung]** listet alle Eigenschaften des Formulars auf, die Steuerelementen auf der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die zum Suchen des Formulars verwendet werden. Die **MessageClass-,** **Clsid-** und **DisplayName-Einträge,** die den Namen der Nachrichtenklasse des Formulars, dessen GUID bzw. den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. Die verbleibenden Einträge sind optional. Das Format des **Abschnitts [Beschreibung]** lautet: 
  
Der Abschnitt **[Beschreibung]** listet alle Eigenschaften des Formulars auf, die Steuerelementen auf der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die zum Suchen des Formulars verwendet werden. Die **MessageClass-,** **Clsid-** und **DisplayName-Einträge,** die den Namen der Nachrichtenklasse des Formulars, dessen GUID bzw. den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. Die verbleibenden Einträge sind optional. Das Format des **Abschnitts [Beschreibung]** lautet: 
  
 **[Beschreibung] MessageClass**  =   _zeichenfolge_
  
 **Clsid**  =   _GUID_
  
 **DisplayName**  =   _displayedstring_
  
 **SmallIcon**  =   _Pfad_
  
 **LargeIcon**  =   _Pfad_
  
Optionale Einträge sind:
  
 **Kategorie**  =   _angezeigte Zeichenfolge_
  
 **Unterkategorie**  =   _angezeigte Zeichenfolge_
  
 **Kommentar**  =   _angezeigte Zeichenfolge_
  
 **Besitzer**  =   _angezeigte Zeichenfolge_
  
 **Zahl**  =   _angezeigte Zeichenfolge_
  
 **Version**  =   _ganze Zahl_
  
 **Gebietsschema**  =   _zeichenfolge_
  
 **Ausgeblendet**  =   _ganze Zahl_
  
 **DesignerToolName**  =   _zeichenfolge_
  
 **DesignerToolGuid**  =   _clsid_
  
 **DesignerRuntimeGuid**  =   _clsid_
  
 **ComposeInFolder**  =   _0|1_
  
 **ComposeCommand**  =   _zeichenfolge_
  
Die **Kategorie-** und **Unterkategorieeinträge** werden von Formularinstallationsprogrammen verwendet, um die Standardkategorisierung von Formularen auf der Benutzeroberfläche der Clientanwendung einzurichten. Beispielsweise könnte eine Hierarchie eingerichtet werden, in der "Helpdesk" die Kategorie ist und "Software" und "Hardware" die Unterkategorien sind. Diese Kategorisierung kann dann von Viewer-Anwendungen verwendet werden, um Nachrichten organisierter anzuzeigen. Die Einträge **"Kommentar",** **"Besitzer"** und **"Zahl"** sind alle Kommentarzeichenfolgen, die auf der Benutzeroberfläche der Clientanwendung angezeigt werden. Hierbei handelt es sich um formularspezifische Eigenschaften, die im Ermessen des Formularentwicklers verwendet werden können. Beispielsweise kann der **Kommentareintrag** verwendet werden, um den Zweck des Formulars anzugeben, den **Besitzereintrag,** der verwendet wird, um die Person oder Organisation anzugeben, die für die Verwaltung des Formulars verantwortlich ist, und die Nummer, die zum Nachverfolgen einer anderen Version des Formulars verwendet wird. Für den **Kommentareintrag** können bis zu zehn Kommentarzeilen eingeschlossen werden. In der ersten Kommentarzeile wird das Wort "Kommentar" als Schlüssel verwendet, in der zweiten Zeile von Kommentaren wird "Comment1" als Taste usw. bis "Comment9" verwendet. 
  
Die **Einträge LargeIcon** und **SmallIcon** werden verwendet, um den Pfad für die Symbolressourcen anzugeben, die zum Anzeigen von Symbolen auf der Benutzeroberfläche der Clientanwendung verwendet werden. Dies gilt in der Regel für Tabellenzeilen, die die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) -Eigenschaftsspalten enthalten. Symboldateinamen können als Pfadnamen relativ zu dem Verzeichnis angegeben werden, in dem die Formularkonfigurationsdatei installiert ist. Der **Versionseintrag** wird verwendet, um die Versionsnummer des Formulars anzugeben. **Das Gebietsschema** ist der dreistellige Sprachbezeichner der Zielformularbibliothek. Eine Liste dieser Bezeichner finden Sie in der _Win32-Programmierreferenz._
  
Der **Eintrag "Ausgeblendet"** gibt an, ob das Formular auf der Benutzeroberfläche eines Formularbibliotheksanbieters angezeigt werden soll: 1 gibt an, dass die Datei ausgeblendet ist, und 0 gibt an, dass das Formular sichtbar ist. Nachfolgend sehen Sie ein Beispiel für eine Formularkonfigurationsdatei. 
  
Der **ComposeInFolder-Eintrag** steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers platziert werden soll, wenn der Benutzer die Nachricht beim Verfassen speichert: 1 gibt an, dass das Formular in den aktuellen Ordner verschoben werden soll, und 0 gibt an, dass es im Posteingang abgelegt werden soll. 
  
Der **ComposeCommand-Eintrag** ist die Zeichenfolge, die im Verfassenmenü der Clientanwendung platziert werden soll. Wenn dies nicht angegeben ist, wird der **DisplayName-Eintrag** verwendet. 
  
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


