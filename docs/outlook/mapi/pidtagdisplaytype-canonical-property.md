---
title: Kanonische PidTagDisplayType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360781"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="e214a-103">Kanonische PidTagDisplayType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e214a-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="e214a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e214a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e214a-105">Enthält einen Wert, der zum Zuordnen eines Symbols zu einer bestimmten Zeile einer Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e214a-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e214a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e214a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e214a-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="e214a-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="e214a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e214a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e214a-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="e214a-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="e214a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e214a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e214a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e214a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e214a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e214a-112">Area:</span></span>  <br/> |<span data-ttu-id="e214a-113">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="e214a-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e214a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e214a-114">Remarks</span></span>

<span data-ttu-id="e214a-115">Diese Eigenschaft enthält eine lange ganze Zahl, die eine spezielle Behandlung des Tabelleneintrags basierend auf dem Typ ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e214a-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="e214a-116">Diese spezielle Behandlung besteht in der Regel darin, ein Symbol oder ein anderes Anzeigeelement anzuzeigen, das dem Anzeigetyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e214a-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="e214a-117">Diese Eigenschaft wird nicht in Ordnerinhaltstabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e214a-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="e214a-118">Client Anwendungen sollten die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft einer Nachricht und die entsprechende [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle verwenden, um die **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md)) und **PR_MINI_ICON** abzurufen ([ Pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaften für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e214a-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="e214a-119">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="e214a-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="e214a-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="e214a-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="e214a-121">Ein automatisierter Agent, wie beispielsweise "Quote-of-the-Day"-oder eine Wetter Diagrammanzeige.</span><span class="sxs-lookup"><span data-stu-id="e214a-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="e214a-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="e214a-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="e214a-123">Eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="e214a-123">A distribution list.</span></span>
    
<span data-ttu-id="e214a-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="e214a-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="e214a-125">Standardordner Symbol neben Ordner anzeigen</span><span class="sxs-lookup"><span data-stu-id="e214a-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="e214a-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="e214a-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="e214a-127">Symbol für Standardordner Verknüpfung neben Ordner anstelle des Standardordner Symbols anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e214a-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="e214a-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="e214a-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="e214a-129">Anzeigesymbol für einen Ordner mit anwendungsspezifischer Unterscheidung, beispielsweise einen speziellen öffentlichen Ordnertyp.</span><span class="sxs-lookup"><span data-stu-id="e214a-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="e214a-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="e214a-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="e214a-131">Ein Forum, beispielsweise ein Bulletin Board-Dienst oder ein öffentlicher oder freigegebener Ordner.</span><span class="sxs-lookup"><span data-stu-id="e214a-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="e214a-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="e214a-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="e214a-133">Ein globales Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="e214a-133">A global address book.</span></span>
    
<span data-ttu-id="e214a-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="e214a-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="e214a-135">Ein lokales Adressbuch, das Sie für eine kleine Arbeitsgruppe freigeben.</span><span class="sxs-lookup"><span data-stu-id="e214a-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="e214a-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="e214a-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="e214a-137">Ein typischer Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="e214a-137">A typical messaging user.</span></span>
    
<span data-ttu-id="e214a-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="e214a-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="e214a-139">Änderbaren der Container sollte in der Benutzeroberfläche als veränderbar gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e214a-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="e214a-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="e214a-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="e214a-141">Stimmt mit keiner der anderen Einstellungen überein.</span><span class="sxs-lookup"><span data-stu-id="e214a-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="e214a-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="e214a-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="e214a-143">Ein spezieller Alias, der für eine umfangreiche Gruppe definiert wurde, beispielsweise Helpdesk, Accounting oder Blood-Drive Coordinator.</span><span class="sxs-lookup"><span data-stu-id="e214a-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="e214a-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="e214a-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="e214a-145">Eine private, persönlich verwaltete Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="e214a-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="e214a-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="e214a-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="e214a-147">Ein Empfänger, der bekanntermaßen von einem fremd-oder Remote Messagingsystem stammt.</span><span class="sxs-lookup"><span data-stu-id="e214a-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="e214a-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="e214a-148">DT_WAN</span></span> 
  
> <span data-ttu-id="e214a-149">Ein Wide Area Network-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="e214a-149">A wide area network address book.</span></span>
    
<span data-ttu-id="e214a-150">In den Adressbuch Inhaltstabellen werden die Werte DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST und DT_REMOTE_MAILUSER verwendet.</span><span class="sxs-lookup"><span data-stu-id="e214a-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="e214a-151">Adressbuch-Hierarchietabellen und einmalige Tabellen verwenden Sie die Werte DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC und DT_WAN.</span><span class="sxs-lookup"><span data-stu-id="e214a-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="e214a-152">Ordner Hierarchietabellen verwenden die DT_FOLDER-, DT_FOLDER_LINK-und DT_FOLDER_SPECIAL-Werte.</span><span class="sxs-lookup"><span data-stu-id="e214a-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="e214a-153">Wenn diese Eigenschaft nicht festgelegt ist, sollte der Client den für die Tabelle geeigneten Standardtyp annehmen, in der Regel DT_FOLDER, DT_LOCAL oder DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="e214a-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="e214a-154">**Hinweis** Alle nicht dokumentierten Werte sind für MAPI reserviert.</span><span class="sxs-lookup"><span data-stu-id="e214a-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="e214a-155">Client Anwendungen dürfen keine neuen Werte definieren und müssen auf den Umgang mit einem nicht dokumentierten Wert vorbereitet sein.</span><span class="sxs-lookup"><span data-stu-id="e214a-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e214a-156">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e214a-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e214a-157">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e214a-157">Protocol specifications</span></span>

<span data-ttu-id="e214a-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e214a-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e214a-159">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e214a-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e214a-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e214a-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e214a-161">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e214a-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e214a-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e214a-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e214a-163">Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e214a-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="e214a-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e214a-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e214a-165">Aktiviert den Verzeichniszugriff.</span><span class="sxs-lookup"><span data-stu-id="e214a-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e214a-166">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e214a-166">Header files</span></span>

<span data-ttu-id="e214a-167">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e214a-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="e214a-168">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e214a-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="e214a-169">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e214a-169">Mapitags.h</span></span>
  
> <span data-ttu-id="e214a-170">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e214a-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e214a-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e214a-171">See also</span></span>



[<span data-ttu-id="e214a-172">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e214a-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e214a-173">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e214a-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e214a-174">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e214a-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e214a-175">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e214a-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

