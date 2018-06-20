---
title: Anzeige Server Ordner Größen-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1ddf4501918d598169a3a74fd1c8d2ac38499cd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791552"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="01b23-103">Anzeige Server Ordner Größen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01b23-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="01b23-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01b23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01b23-105">Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook- **Ordner-Größe** .</span><span class="sxs-lookup"><span data-stu-id="01b23-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="01b23-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="01b23-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01b23-107">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="01b23-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="01b23-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt</span><span class="sxs-lookup"><span data-stu-id="01b23-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="01b23-109">Erstellt:</span><span class="sxs-lookup"><span data-stu-id="01b23-109">Created by:</span></span>  <br/> |<span data-ttu-id="01b23-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="01b23-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="01b23-111">Durch zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="01b23-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="01b23-112">Outlook und andere clients</span><span class="sxs-lookup"><span data-stu-id="01b23-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="01b23-113">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="01b23-113">Property type:</span></span>  <br/> |<span data-ttu-id="01b23-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="01b23-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="01b23-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="01b23-115">Access type:</span></span>  <br/> |<span data-ttu-id="01b23-116">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="01b23-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01b23-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01b23-117">Remarks</span></span>

<span data-ttu-id="01b23-118">Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="01b23-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="01b23-119">Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="01b23-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="01b23-120">[HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="01b23-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="01b23-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="01b23-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="01b23-122">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="01b23-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01b23-123">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="01b23-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="01b23-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="01b23-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="01b23-125">UlKind:</span><span class="sxs-lookup"><span data-stu-id="01b23-125">ulKind:</span></span>  <br/> |<span data-ttu-id="01b23-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="01b23-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="01b23-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="01b23-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="01b23-128">L "Urn: Schemas-Microsoft-Com:office:outlook #serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="01b23-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="01b23-129">Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01b23-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="01b23-130">Wenn die Version von Outlook einer älteren Version als Outlook 2003 SP 1 ist, oder wenn der Wert **false**lautet, Outlook nur die Größe der Ordner auf dem lokalen Speicher zeigt.</span><span class="sxs-lookup"><span data-stu-id="01b23-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="01b23-131">Wenn diese Eigenschaft in einem Speicher festgelegt ist, Outlook 2003 SP 1 verwendet, wird die Größe der einzelnen angegebenen Ordner auf dem Server und dem lokalen Laufwerk Outlook Abfragen.</span><span class="sxs-lookup"><span data-stu-id="01b23-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="01b23-132">Um die Größe des Ordners auf dem Server abzufragen, Outlook wird geöffnet, einen Ordner auf den Speicher mit [IMsgStore::OpenEntry](imsgstore-openentry.md), übergeben die Kennzeichen **MAPI_NO_CACHE**, und fragt dann **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="01b23-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="01b23-133">Der Anbieter sollte die Größe des Ordners klicken Sie dann auf dem Server zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01b23-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="01b23-134">Um die Größe eines Ordners auf dem lokalen Laufwerk abzufragen, öffnet Outlook den Ordner ohne das **MAPI_NO_CACHE** -Flag.</span><span class="sxs-lookup"><span data-stu-id="01b23-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="01b23-135">Anschließend fragt **PR_MESSAGE_SIZE_EXTENDED**; der Anbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="01b23-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="01b23-136">Diese Eigenschaft festgelegt ist können Anbieter, die Store Inhalt auf einen Server synchronisieren Ordner Größendaten auf dem Server im Dialogfeld Outlook- **Größe des Ordners** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="01b23-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="01b23-137">Benutzer können ihre aktuellen Server Speicherplatzverwendung mit Vorgaben Server verglichen.</span><span class="sxs-lookup"><span data-stu-id="01b23-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

