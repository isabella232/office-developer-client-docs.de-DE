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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433094"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="623f2-103">Formular Konfigurationsdatei [Beschreibung] Abschnitt</span><span class="sxs-lookup"><span data-stu-id="623f2-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="623f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="623f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="623f2-105">Der Abschnitt **[Description]** enthält alle Eigenschaften des Formulars, die Steuerelementen in der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die beim Auffinden des Formulars verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="623f2-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="623f2-106">Die **MessageClass**-, **CLSID**-und **Display** Name-Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. .</span><span class="sxs-lookup"><span data-stu-id="623f2-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="623f2-107">Die restlichen Einträge sind optional.</span><span class="sxs-lookup"><span data-stu-id="623f2-107">The remaining entries are optional.</span></span> <span data-ttu-id="623f2-108">Das Format des Abschnitts **[Description]** lautet:</span><span class="sxs-lookup"><span data-stu-id="623f2-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="623f2-109">Der Abschnitt **[Description]** enthält alle Eigenschaften des Formulars, die Steuerelementen in der Benutzeroberfläche des Formulars zugeordnet sind, sowie Attribute, die beim Auffinden des Formulars verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="623f2-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="623f2-110">Die **MessageClass**-, **CLSID**-und **Display** Name-Einträge, die den Namen der Nachrichtenklasse des Formulars, dessen GUID und den Anzeigenamen der Nachrichtenklasse identifizieren, sind erforderliche Einträge, die zum Suchen des Formulars in der Formularbibliothek verwendet werden. .</span><span class="sxs-lookup"><span data-stu-id="623f2-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="623f2-111">Die restlichen Einträge sind optional.</span><span class="sxs-lookup"><span data-stu-id="623f2-111">The remaining entries are optional.</span></span> <span data-ttu-id="623f2-112">Das Format des Abschnitts **[Description]** lautet:</span><span class="sxs-lookup"><span data-stu-id="623f2-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="623f2-113">**Beschreibung MessageClass** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="623f2-114">**CLSID** =  -_GUID_</span><span class="sxs-lookup"><span data-stu-id="623f2-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="623f2-115">\*\*\*\* =  _Anzeige_ Name</span><span class="sxs-lookup"><span data-stu-id="623f2-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="623f2-116">**SmallIcon** =  -_Pfad_</span><span class="sxs-lookup"><span data-stu-id="623f2-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="623f2-117">**LargeIcon** =  -_Pfad_</span><span class="sxs-lookup"><span data-stu-id="623f2-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="623f2-118">Optionale Einträge sind:</span><span class="sxs-lookup"><span data-stu-id="623f2-118">Optional entries are:</span></span>
  
 <span data-ttu-id="623f2-119">**Kategorie** =  _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="623f2-120">**Unterkategorie** =  _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="623f2-121">**Kommentar** =  _angezeigte Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="623f2-122">\*\*\*\* =  _Angezeigte Zeichenfolge_ des Besitzers</span><span class="sxs-lookup"><span data-stu-id="623f2-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="623f2-123">\*\*\*\* Angezeigte Zeichen_Folge_  =  </span><span class="sxs-lookup"><span data-stu-id="623f2-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="623f2-124">\*\*\*\* =  _Ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="623f2-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="623f2-125">**Gebietsschema** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="623f2-126">**Ausgeblendete** =  _Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="623f2-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="623f2-127">**DesignerToolName** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="623f2-128">**DesignerToolGuid** =  -_CLSID_</span><span class="sxs-lookup"><span data-stu-id="623f2-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="623f2-129">**DesignerRuntimeGuid** =  -_CLSID_</span><span class="sxs-lookup"><span data-stu-id="623f2-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="623f2-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="623f2-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="623f2-131">**ComposeCommand** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="623f2-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="623f2-132">Die Einträge **Category** und SubCategory werden von Formular Installationsprogrammen verwendet, um die Standard Kategorisierung von Formularen in der Benutzeroberfläche der Clientanwendung einzurichten. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="623f2-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="623f2-133">Beispielsweise könnte eine Hierarchie eingerichtet werden, in der "Help Desk" die Kategorie und "Software" und "Hardware" waren die Unterkategorien.</span><span class="sxs-lookup"><span data-stu-id="623f2-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="623f2-134">Diese Kategorisierung kann dann von Viewer-Anwendungen verwendet werden, um Nachrichten auf eine strukturiertere Weise anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="623f2-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="623f2-135">Die Einträge **Kommentar**, **Besitzer**und **Anzahl** sind alle Kommentarzeichenfolgen, die auf der Benutzeroberfläche der Clientanwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="623f2-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="623f2-136">Hierbei handelt es sich um formularspezifische Eigenschaften, die nach Ermessen des Formular Entwicklers verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="623f2-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="623f2-137">Der **Kommentar** Eintrag kann beispielsweise verwendet werden, um den Zweck des Formulars anzugeben, den **Besitzer** Eintrag, der die Person oder Organisation angibt, die für die Verwaltung des Formulars zuständig ist, und die Nummer, die zum Nachverfolgen der verschiedenen Formularversionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="623f2-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="623f2-138">Für den **Kommentar** Eintrag können bis zu zehn Zeilen mit Kommentaren enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="623f2-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="623f2-139">Die erste Codezeile verwendet das Wort "comment" als Schlüssel, in der zweiten Kommentar Reihe wird "Comment1" als Schlüssel verwendet, und so weiter über "Comment9".</span><span class="sxs-lookup"><span data-stu-id="623f2-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="623f2-140">Die **LargeIcon** -und **SmallIcon** -Einträge werden verwendet, um den Pfad für die Symbolressourcen anzugeben, die zum Anzeigen der Symbole in der Benutzeroberfläche der Clientanwendung verwendet werden, in der Regel für Tabellenzeilen, die das **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaftsspalten.</span><span class="sxs-lookup"><span data-stu-id="623f2-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="623f2-141">Symboldateinamen können als Pfadnamen relativ zu dem Verzeichnis angegeben werden, in dem die Formular Konfigurationsdatei installiert ist.</span><span class="sxs-lookup"><span data-stu-id="623f2-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="623f2-142">Der **Versions** Eintrag wird verwendet, um die Versionsnummer des Formulars anzugeben.</span><span class="sxs-lookup"><span data-stu-id="623f2-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="623f2-143">**Locale** ist der Sprachenbezeichner aus drei Buchstaben der Zielformular Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="623f2-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="623f2-144">Eine Liste dieser Bezeichner finden Sie unter _Win32 Programmer es Reference_.</span><span class="sxs-lookup"><span data-stu-id="623f2-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="623f2-145">Der **Ausgeblendete** Eintrag gibt an, ob das Formular in der Benutzeroberfläche eines Formularbibliothek Anbieters angezeigt werden soll: 1 gibt an, dass die Datei ausgeblendet ist, und 0 gibt an, dass das Formular sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="623f2-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="623f2-146">Nachfolgend sehen Sie eine Beispiel-Formular Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="623f2-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="623f2-147">Der **ComposeInFolder** -Eintrag steuert, ob das Formular im aktuellen Ordner oder im Posteingang des Benutzers abgelegt werden soll, wenn der Benutzer die Nachricht beim Erstellen speichert: 1 gibt an, dass das Formular in den aktuellen Ordner verschoben werden soll, und 0 gibt an, dass es Wechseln Sie in den Posteingang.</span><span class="sxs-lookup"><span data-stu-id="623f2-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="623f2-148">Der **ComposeCommand** -Eintrag ist die Zeichenfolge, die im Verfassen-Menü der Clientanwendung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="623f2-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="623f2-149">Wenn dies nicht angegeben wird, wird der Eintrag **DisplayName** verwendet.</span><span class="sxs-lookup"><span data-stu-id="623f2-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


