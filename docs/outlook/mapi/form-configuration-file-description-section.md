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
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="9e478-103">Abschnitt "Formularkonfigurationsdatei" [Beschreibung]</span><span class="sxs-lookup"><span data-stu-id="9e478-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="9e478-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e478-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e478-105">Im **Abschnitt [Beschreibung]** werden alle Eigenschaften des Formulars aufgeführt, die Steuerelementen auf der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die zum Suchen des Formulars verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e478-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="9e478-106">Die **Einträge MessageClass**, Clsid und **DisplayName,** die den Namen der Nachrichtenklasse des **Formulars,** die GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e478-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="9e478-107">Die verbleibenden Einträge sind optional.</span><span class="sxs-lookup"><span data-stu-id="9e478-107">The remaining entries are optional.</span></span> <span data-ttu-id="9e478-108">Das Format des **Abschnitts [Beschreibung]** ist:</span><span class="sxs-lookup"><span data-stu-id="9e478-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="9e478-109">Im **Abschnitt [Beschreibung]** werden alle Eigenschaften des Formulars aufgeführt, die Steuerelementen auf der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die zum Suchen des Formulars verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e478-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="9e478-110">Die **Einträge MessageClass**, Clsid und **DisplayName,** die den Namen der Nachrichtenklasse des **Formulars,** die GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e478-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="9e478-111">Die verbleibenden Einträge sind optional.</span><span class="sxs-lookup"><span data-stu-id="9e478-111">The remaining entries are optional.</span></span> <span data-ttu-id="9e478-112">Das Format des **Abschnitts [Beschreibung]** ist:</span><span class="sxs-lookup"><span data-stu-id="9e478-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="9e478-113">**[Beschreibung] MessageClass**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="9e478-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="9e478-114">**Clsid**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="9e478-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="9e478-115">**DisplayName**  =   _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="9e478-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="9e478-116">**SmallIcon**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="9e478-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="9e478-117">**LargeIcon**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="9e478-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="9e478-118">Optionale Einträge sind:</span><span class="sxs-lookup"><span data-stu-id="9e478-118">Optional entries are:</span></span>
  
 <span data-ttu-id="9e478-119">**Kategorie**  =   _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="9e478-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="9e478-120">**Unterkategorie**  =   _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="9e478-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="9e478-121">**Kommentar**  =   _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="9e478-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="9e478-122">**Besitzer**  =   _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="9e478-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="9e478-123">**Number**  =   _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="9e478-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="9e478-124">**Version**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="9e478-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="9e478-125">**Locale**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="9e478-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="9e478-126">**Ausgeblendet**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="9e478-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="9e478-127">**DesignerToolName**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="9e478-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="9e478-128">**DesignerToolGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="9e478-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="9e478-129">**DesignerRuntimeGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="9e478-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="9e478-130">**ComposeInFolder**  =   _0|1_</span><span class="sxs-lookup"><span data-stu-id="9e478-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="9e478-131">**ComposeCommand**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="9e478-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="9e478-132">Die **Einträge Category** und **Unterkategorie** werden von Formularinstallationsmodulen verwendet, um die Standardkategorisierung von Formularen auf der Benutzeroberfläche der Clientanwendung zu einrichten.</span><span class="sxs-lookup"><span data-stu-id="9e478-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="9e478-133">Beispielsweise könnte eine Hierarchie eingerichtet werden, bei der "Help Desk" die Kategorie und "Software" und "Hardware" die Unterkategorien waren.</span><span class="sxs-lookup"><span data-stu-id="9e478-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="9e478-134">Diese Kategorisierung kann dann von Vieweranwendungen verwendet werden, um Nachrichten besser organisiert zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="9e478-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="9e478-135">Die **Einträge Comment**, **Owner** und **Number** sind alle Kommentarzeichenfolgen, die auf der Benutzeroberfläche der Clientanwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e478-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="9e478-136">Dies sind formularspezifische Eigenschaften, die nach Ermessen des Formularentwicklers verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e478-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="9e478-137">Beispielsweise kann der **Kommentareintrag** verwendet werden, um den Zweck des Formulars anzugeben, den **Besitzereintrag,** der verwendet wird, um die Person oder Organisation anzugeben, die für die Verwaltung des Formulars verantwortlich ist, und die Nummer, die zum Nachverfolgen einer anderen Version des Formulars verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e478-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="9e478-138">Für den **Kommentareintrag** können bis zu zehn Kommentarzeilen eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9e478-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="9e478-139">In der ersten Kommentarzeile wird das Wort "Comment" als Schlüssel verwendet, in der zweiten Kommentarzeile wird "Comment1" als Schlüssel verwendet, und so weiter über "Comment9".</span><span class="sxs-lookup"><span data-stu-id="9e478-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="9e478-140">Die **Einträge LargeIcon** und **SmallIcon** werden verwendet, um den Pfad für die Symbolressourcen anzugeben, die zum Anzeigen von Symbolen auf der Benutzeroberfläche der Clientanwendung verwendet werden. Dies gilt in der Regel für Tabellenzeilen, die die **Eigenschaftenspalten PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e478-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="9e478-141">Symboldateinamen können als Pfadnamen relativ zum Verzeichnis angegeben werden, in dem die Formularkonfigurationsdatei installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e478-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="9e478-142">Der **Eintrag Version** wird verwendet, um die Versionsnummer des Formulars anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9e478-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="9e478-143">**Locale** ist der Drei-Buchstaben-Sprachbezeichner der Zielformularbibliothek.</span><span class="sxs-lookup"><span data-stu-id="9e478-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="9e478-144">Eine Liste dieser Bezeichner finden Sie im  _Win32 Programmer's Reference_.</span><span class="sxs-lookup"><span data-stu-id="9e478-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="9e478-145">Der **Eintrag Ausgeblendet** gibt an, ob das Formular auf der Benutzeroberfläche eines Formularbibliotheksanbieters angezeigt werden soll: 1 gibt an, dass die Datei ausgeblendet ist, und 0 gibt an, dass das Formular sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="9e478-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="9e478-146">Im Folgenden wird eine Beispielkonfigurationsdatei gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e478-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="9e478-147">Der **ComposeInFolder-Eintrag** steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers platziert werden soll, wenn der Benutzer die Nachricht beim Verfassen speichert: 1 gibt an, dass das Formular in den aktuellen Ordner und 0 in den Posteingang wechseln soll.</span><span class="sxs-lookup"><span data-stu-id="9e478-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="9e478-148">Der **Eintrag ComposeCommand** ist die Zeichenfolge, die im Verfassenmenü der Clientanwendung platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e478-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="9e478-149">Wenn dies nicht angegeben ist, wird der **DisplayName-Eintrag** verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e478-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


