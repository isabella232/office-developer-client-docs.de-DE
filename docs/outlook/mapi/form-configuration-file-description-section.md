---
title: Abschnitt "Formularkonfigurationsdatei" [Beschreibung]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433094"
---
# <a name="form-configuration-file-description-section"></a>Abschnitt "Formularkonfigurationsdatei" [Beschreibung]
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Beschreibung]** werden alle Eigenschaften des Formulars aufgeführt, die Steuerelementen auf der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die zum Suchen des Formulars verwendet werden. Die **Einträge MessageClass**, Clsid und **DisplayName,** die den Namen der Nachrichtenklasse des **Formulars,** die GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. Die verbleibenden Einträge sind optional. Das Format des **Abschnitts [Beschreibung]** ist: 
  
Im **Abschnitt [Beschreibung]** werden alle Eigenschaften des Formulars aufgeführt, die Steuerelementen auf der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die zum Suchen des Formulars verwendet werden. Die **Einträge MessageClass**, Clsid und **DisplayName,** die den Namen der Nachrichtenklasse des **Formulars,** die GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. Die verbleibenden Einträge sind optional. Das Format des **Abschnitts [Beschreibung]** ist: 
  
 **[Beschreibung] MessageClass**  =   _string_
  
 **Clsid**  =   _guid_
  
 **DisplayName**  =   _displayedstring_
  
 **SmallIcon**  =   _path_
  
 **LargeIcon**  =   _path_
  
Optionale Einträge sind:
  
 **Kategorie**  =   _angezeigte Zeichenfolge_
  
 **Unterkategorie**  =   _angezeigte Zeichenfolge_
  
 **Kommentar**  =   _angezeigte Zeichenfolge_
  
 **Besitzer**  =   _angezeigte Zeichenfolge_
  
 **Number**  =   _angezeigte Zeichenfolge_
  
 **Version**  =   _integer_
  
 **Locale**  =   _string_
  
 **Ausgeblendet**  =   _integer_
  
 **DesignerToolName**  =   _string_
  
 **DesignerToolGuid**  =   _clsid_
  
 **DesignerRuntimeGuid**  =   _clsid_
  
 **ComposeInFolder**  =   _0|1_
  
 **ComposeCommand**  =   _string_
  
Die **Einträge Category** und **Unterkategorie** werden von Formularinstallationsmodulen verwendet, um die Standardkategorisierung von Formularen auf der Benutzeroberfläche der Clientanwendung zu einrichten. Beispielsweise könnte eine Hierarchie eingerichtet werden, bei der "Help Desk" die Kategorie und "Software" und "Hardware" die Unterkategorien waren. Diese Kategorisierung kann dann von Vieweranwendungen verwendet werden, um Nachrichten besser organisiert zu zeigen. Die **Einträge Comment**, **Owner** und **Number** sind alle Kommentarzeichenfolgen, die auf der Benutzeroberfläche der Clientanwendung angezeigt werden. Dies sind formularspezifische Eigenschaften, die nach Ermessen des Formularentwicklers verwendet werden können. Beispielsweise kann der **Kommentareintrag** verwendet werden, um den Zweck des Formulars anzugeben, den **Besitzereintrag,** der verwendet wird, um die Person oder Organisation anzugeben, die für die Verwaltung des Formulars verantwortlich ist, und die Nummer, die zum Nachverfolgen einer anderen Version des Formulars verwendet wird. Für den **Kommentareintrag** können bis zu zehn Kommentarzeilen eingeschlossen werden. In der ersten Kommentarzeile wird das Wort "Comment" als Schlüssel verwendet, in der zweiten Kommentarzeile wird "Comment1" als Schlüssel verwendet, und so weiter über "Comment9". 
  
Die **Einträge LargeIcon** und **SmallIcon** werden verwendet, um den Pfad für die Symbolressourcen anzugeben, die zum Anzeigen von Symbolen auf der Benutzeroberfläche der Clientanwendung verwendet werden. Dies gilt in der Regel für Tabellenzeilen, die die **Eigenschaftenspalten PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) enthalten. Symboldateinamen können als Pfadnamen relativ zum Verzeichnis angegeben werden, in dem die Formularkonfigurationsdatei installiert ist. Der **Eintrag Version** wird verwendet, um die Versionsnummer des Formulars anzugeben. **Locale** ist der Drei-Buchstaben-Sprachbezeichner der Zielformularbibliothek. Eine Liste dieser Bezeichner finden Sie im  _Win32 Programmer's Reference_.
  
Der **Eintrag Ausgeblendet** gibt an, ob das Formular auf der Benutzeroberfläche eines Formularbibliotheksanbieters angezeigt werden soll: 1 gibt an, dass die Datei ausgeblendet ist, und 0 gibt an, dass das Formular sichtbar ist. Im Folgenden wird eine Beispielkonfigurationsdatei gezeigt. 
  
Der **ComposeInFolder-Eintrag** steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers platziert werden soll, wenn der Benutzer die Nachricht beim Verfassen speichert: 1 gibt an, dass das Formular in den aktuellen Ordner und 0 in den Posteingang wechseln soll. 
  
Der **Eintrag ComposeCommand** ist die Zeichenfolge, die im Verfassenmenü der Clientanwendung platziert werden soll. Wenn dies nicht angegeben ist, wird der **DisplayName-Eintrag** verwendet. 
  
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


