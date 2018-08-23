---
title: Abschnitt [Description] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ad5fd9cf437afc3999697792850548e4e5a1435
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582896"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="cba67-103">Abschnitt [Description] in der Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="cba67-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="cba67-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cba67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cba67-105">Im Abschnitt **[Beschreibung]** enthält alle Eigenschaften des Formulars, die Steuerelemente in des Formulars die Benutzeroberfläche und Attribute, die verwendet werden, bei der Suche nach dem Formular zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cba67-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="cba67-106">Die **MessageClass**, **Clsid**und **DisplayName** -Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und die Nachrichtenklasse Anzeigename, jeweils zu identifizieren, sind erforderliche Einträge verwendet, um das Formular in der Formularbibliothek gesucht werden soll. .</span><span class="sxs-lookup"><span data-stu-id="cba67-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="cba67-107">Die verbleibenden Einträge sind optional.</span><span class="sxs-lookup"><span data-stu-id="cba67-107">The remaining entries are optional.</span></span> <span data-ttu-id="cba67-108">Das Format des Abschnitts **[Beschreibung]** lautet:</span><span class="sxs-lookup"><span data-stu-id="cba67-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="cba67-109">Im Abschnitt **[Beschreibung]** enthält alle Eigenschaften des Formulars, die Steuerelemente in des Formulars die Benutzeroberfläche und Attribute, die verwendet werden, bei der Suche nach dem Formular zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cba67-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="cba67-110">Die **MessageClass**, **Clsid**und **DisplayName** -Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und die Nachrichtenklasse Anzeigename, jeweils zu identifizieren, sind erforderliche Einträge verwendet, um das Formular in der Formularbibliothek gesucht werden soll. .</span><span class="sxs-lookup"><span data-stu-id="cba67-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="cba67-111">Die verbleibenden Einträge sind optional.</span><span class="sxs-lookup"><span data-stu-id="cba67-111">The remaining entries are optional.</span></span> <span data-ttu-id="cba67-112">Das Format des Abschnitts **[Beschreibung]** lautet:</span><span class="sxs-lookup"><span data-stu-id="cba67-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="cba67-113">**[Beschreibung] MessageClass** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="cba67-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="cba67-114">**CLSID** =  _Guid_</span><span class="sxs-lookup"><span data-stu-id="cba67-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="cba67-115">**DisplayName** =  _Displayedstring_</span><span class="sxs-lookup"><span data-stu-id="cba67-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="cba67-116">**SmallIcon** =  _Pfad_</span><span class="sxs-lookup"><span data-stu-id="cba67-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="cba67-117">**LargeIcon** =  _Pfad_</span><span class="sxs-lookup"><span data-stu-id="cba67-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="cba67-118">Optionale Einträge sind:</span><span class="sxs-lookup"><span data-stu-id="cba67-118">Optional entries are:</span></span>
  
 <span data-ttu-id="cba67-119">**Kategorie** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="cba67-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="cba67-120">**Unterkategorie** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="cba67-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="cba67-121">**Kommentar** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="cba67-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="cba67-122">**Besitzer** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="cba67-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="cba67-123">**Anzahl** =  _Zeichenfolge angezeigt_</span><span class="sxs-lookup"><span data-stu-id="cba67-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="cba67-124">**Version** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="cba67-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="cba67-125">**Gebietsschema** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="cba67-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="cba67-126">**Ausgeblendete** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="cba67-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="cba67-127">**DesignerToolName** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="cba67-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="cba67-128">**DesignerToolGuid** =  _Clsid_</span><span class="sxs-lookup"><span data-stu-id="cba67-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="cba67-129">**DesignerRuntimeGuid** =  _Clsid_</span><span class="sxs-lookup"><span data-stu-id="cba67-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="cba67-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="cba67-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="cba67-131">**ComposeCommand** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="cba67-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="cba67-132">Die **Kategorie** und eine **Unterkategorie** Einträge werden vom Formular Installer zum Einrichten der standardmäßigen Kategorisierung von Formularen in die Benutzeroberfläche für Client-Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cba67-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="cba67-133">Beispiel eine Hierarchie konnte eingerichtet werden, auf dem "Help Desk" für die Kategorie ist und "Software" und "Hardware" wurden die Unterkategorien aus.</span><span class="sxs-lookup"><span data-stu-id="cba67-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="cba67-134">Diese Kategorisierung kann dann von Clientanwendungen Viewer zum Anzeigen von Nachrichten in übersichtlicher Weise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cba67-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="cba67-135">Die **Kommentar**, **Besitzer**und die **Anzahl** der Einträge sind alle Kommentarzeichenfolgen, die in der Benutzeroberfläche der Anwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cba67-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="cba67-136">Dies sind bestimmte Formulareigenschaften im Ermessen des Entwicklers Formular verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cba67-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="cba67-137">Beispielsweise kann der Eintrag **Kommentar** an den Zweck des Formulars, den **Besitzer** Eintrag verwendet, um die Person oder Organisation verantwortlich für die Verwaltung des Formulars anzuzeigen und die Anzahl verwendet, um eine andere Version des Formulars Nachverfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cba67-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="cba67-138">Für den **Kommentar** kann bis zu 10 Textzeilen Kommentare-Eintrag eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cba67-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="cba67-139">Die erste Zeile des Kommentare wird das Wort "Comment" als Schlüssel verwendet, die zweite Zeile von Kommentaren verwendet "Comment1" als Schlüssel, und so weiter bis "Comment9."</span><span class="sxs-lookup"><span data-stu-id="cba67-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="cba67-140">Die Einträge **LargeIcon** und **SmallIcon** dienen zum Angeben des Pfads für die Symbolressourcen verwendet, um die Symbole in der Clientanwendung-Benutzeroberfläche angezeigt, in der Regel ist dies für die Zeilen, in denen die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder Spalten für **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cba67-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="cba67-141">Symbol Dateinamen können als Pfadnamen relativ zu dem Verzeichnis angegeben werden, in die Konfigurationsdatei Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cba67-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="cba67-142">Der Eintrag **Version** wird verwendet, um die Versionsnummer des Formulars anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cba67-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="cba67-143">**Gebietsschema** ist die drei Buchstaben bestehende Sprach-ID der Formularbibliothek Ziel.</span><span class="sxs-lookup"><span data-stu-id="cba67-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="cba67-144">Eine Liste dieser Bezeichner finden Sie in der _Win32 Programmer's Reference_.</span><span class="sxs-lookup"><span data-stu-id="cba67-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="cba67-145">Der **Hidden** -Eintrag gibt an, ob das Formular in ein Formular Bibliotheksanbieter-Benutzeroberfläche angezeigt werden sollen: 1 bedeutet, dass die Datei ist ausgeblendet, und 0 bedeutet, dass das Formular sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="cba67-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="cba67-146">Eine Beispielkonfigurationsdatei Formular wird nach angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cba67-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="cba67-147">Der Eintrag **ComposeInFolder** steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers platziert werden, wenn der Benutzer die Nachricht beim Verfassen sie speichert entwickelt wurde: 1 bedeutet, dass das Formular im aktuellen Ordner sollten und 0 bedeutet, dass es sollten Wechseln Sie im Posteingang.</span><span class="sxs-lookup"><span data-stu-id="cba67-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="cba67-148">Der **ComposeCommand** -Eintrag ist die Zeichenfolge, die in der Clientanwendung platziert werden die im Menü verfassen.</span><span class="sxs-lookup"><span data-stu-id="cba67-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="cba67-149">Wenn dies nicht angegeben wird, wird der Eintrag **"DisplayName"** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cba67-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


