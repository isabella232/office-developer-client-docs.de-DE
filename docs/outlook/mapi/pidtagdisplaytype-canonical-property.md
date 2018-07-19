---
title: PidTagDisplayType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3fd5a8d92621dcefce66fb42e843f78755fa84df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794330"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="1f541-103">PidTagDisplayType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f541-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="1f541-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f541-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f541-105">Enthält einen Wert zum Verknüpfen eines Symbols mit einer bestimmten Zeile einer Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f541-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f541-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1f541-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f541-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f541-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="1f541-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1f541-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f541-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="1f541-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="1f541-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1f541-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f541-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f541-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1f541-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1f541-112">Area:</span></span>  <br/> |<span data-ttu-id="1f541-113">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="1f541-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f541-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f541-114">Remarks</span></span>

<span data-ttu-id="1f541-115">Diese Eigenschaft enthält eine lange Ganzzahl, die eine besondere Behandlung des Eintrags Tabelle basierend auf dieses Typs vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1f541-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="1f541-116">Diese besondere Behandlung umfasst in der Regel ein Symbol oder andere Display-Element, den Anzeigetyp zugeordnete anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1f541-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="1f541-117">Diese Eigenschaft wird nicht im Ordner Inhalt Tabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f541-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="1f541-118">Clientanwendungen sollte einer Meldung **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft und entsprechende [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle verwenden, um die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und **PR_MINI_ICON** ([ zu erhalten PidTagMiniIcon](pidtagminiicon-canonical-property.md)) Eigenschaften für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1f541-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="1f541-119">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="1f541-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="1f541-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="1f541-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="1f541-121">Agent automatisierte wie Angebot des Tages oder eine Diagrammanzeige Wetter.</span><span class="sxs-lookup"><span data-stu-id="1f541-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="1f541-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="1f541-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="1f541-123">Eine Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="1f541-123">A distribution list.</span></span>
    
<span data-ttu-id="1f541-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="1f541-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="1f541-125">Standard-Ordnersymbol neben der Ordner anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1f541-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="1f541-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="1f541-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="1f541-127">Zeigt Ordner Link Standardsymbol neben der Ordner, sondern das Standardsymbol für Ordner.</span><span class="sxs-lookup"><span data-stu-id="1f541-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="1f541-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="1f541-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="1f541-129">Zeigt das Symbol für einen Ordner mit einer anwendungsspezifischen Unterschied, wie etwa eine besondere Art des öffentlichen Ordners.</span><span class="sxs-lookup"><span data-stu-id="1f541-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="1f541-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="1f541-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="1f541-131">Foren, wie ein Bulletin Board-Dienst oder ein öffentlicher oder freigegebener Ordner.</span><span class="sxs-lookup"><span data-stu-id="1f541-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="1f541-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="1f541-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="1f541-133">Ein globales Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="1f541-133">A global address book.</span></span>
    
<span data-ttu-id="1f541-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="1f541-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="1f541-135">Eine lokale Adressbuch, das für eine kleine Arbeitsgruppe freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1f541-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="1f541-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="1f541-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="1f541-137">Normaler Benutzer messaging.</span><span class="sxs-lookup"><span data-stu-id="1f541-137">A typical messaging user.</span></span>
    
<span data-ttu-id="1f541-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="1f541-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="1f541-139">Änderbare; der Container sollte in der Benutzeroberfläche als änderbare gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="1f541-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="1f541-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="1f541-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="1f541-141">Stimmt mit keinem der anderen Einstellungen überein.</span><span class="sxs-lookup"><span data-stu-id="1f541-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="1f541-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="1f541-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="1f541-143">Eine spezielle Alias für eine große Gruppe wie Helpdesk, Buchhaltung oder Blut Laufwerk Coordinator definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f541-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="1f541-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="1f541-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="1f541-145">Eine Private, persönlich verwaltet Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="1f541-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="1f541-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="1f541-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="1f541-147">Ein Empfänger bekanntermaßen aus einem fremden oder remote-messaging-System.</span><span class="sxs-lookup"><span data-stu-id="1f541-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="1f541-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="1f541-148">DT_WAN</span></span> 
  
> <span data-ttu-id="1f541-149">Der Adressbuch eines WAN-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1f541-149">A wide area network address book.</span></span>
    
<span data-ttu-id="1f541-150">Address Book Inhalt Tabellen verwenden Sie die Werte DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST und DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="1f541-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="1f541-151">Verwenden Sie die Werte DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC und DT_WAN, Address Book Hierarchietabellen und einmaligen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="1f541-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="1f541-152">Ordner Hierarchietabellen verwenden Sie die Werte DT_FOLDER, DT_FOLDER_LINK und DT_FOLDER_SPECIAL.</span><span class="sxs-lookup"><span data-stu-id="1f541-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="1f541-153">Wenn diese Eigenschaft nicht festgelegt ist, sollte der Client den Standardtyp für die Tabelle, in der Regel DT_FOLDER, DT_LOCAL oder DT_MAILUSER geeignet annehmen.</span><span class="sxs-lookup"><span data-stu-id="1f541-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="1f541-154">**Hinweis** Alle Werte, die nicht dokumentiert sind für die MAPI reserviert.</span><span class="sxs-lookup"><span data-stu-id="1f541-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="1f541-155">Clientanwendungen dürfen Sie keine neue Werte definieren und für den Umgang mit eine nicht dokumentierte Wert vorbereitet sein.</span><span class="sxs-lookup"><span data-stu-id="1f541-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f541-156">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f541-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f541-157">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1f541-157">Protocol specifications</span></span>

<span data-ttu-id="1f541-158">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f541-158">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f541-159">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1f541-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f541-160">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f541-160">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f541-161">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="1f541-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1f541-162">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f541-162">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f541-163">Gibt die Eigenschaften und Operationen, die für Address Book Vorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="1f541-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="1f541-164">[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f541-164">[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f541-165">Verzeichniszugriff wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1f541-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f541-166">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1f541-166">Header files</span></span>

<span data-ttu-id="1f541-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f541-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f541-168">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1f541-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f541-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f541-169">Mapitags.h</span></span>
  
> <span data-ttu-id="1f541-170">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1f541-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f541-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f541-171">See also</span></span>



[<span data-ttu-id="1f541-172">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f541-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f541-173">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f541-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f541-174">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1f541-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f541-175">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1f541-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

