---
title: Display Server Folder Sizes-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434550"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="1976e-103">Display Server Folder Sizes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1976e-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="1976e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1976e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1976e-105">Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook **Ordnergröße** an.</span><span class="sxs-lookup"><span data-stu-id="1976e-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1976e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1976e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1976e-107">Verfügbar gemacht für:</span><span class="sxs-lookup"><span data-stu-id="1976e-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="1976e-108">[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="1976e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="1976e-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="1976e-109">Created by:</span></span>  <br/> |<span data-ttu-id="1976e-110">Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="1976e-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="1976e-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="1976e-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="1976e-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="1976e-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="1976e-113">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="1976e-113">Property type:</span></span>  <br/> |<span data-ttu-id="1976e-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1976e-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1976e-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="1976e-115">Access type:</span></span>  <br/> |<span data-ttu-id="1976e-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1976e-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1976e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1976e-117">Remarks</span></span>

<span data-ttu-id="1976e-118">Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1976e-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="1976e-119">Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1976e-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="1976e-120">Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="1976e-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="1976e-121">Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1976e-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="1976e-122">Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_</span><span class="sxs-lookup"><span data-stu-id="1976e-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1976e-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="1976e-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="1976e-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="1976e-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="1976e-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="1976e-125">ulKind:</span></span>  <br/> |<span data-ttu-id="1976e-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="1976e-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="1976e-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="1976e-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="1976e-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="1976e-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="1976e-129">Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1976e-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="1976e-130">Wenn die Version von Outlook vor Outlook 2003 SP 1 liegt oder der Wert **false** ist, zeigt Outlook nur die Größe der Ordner im lokalen Speicher an.</span><span class="sxs-lookup"><span data-stu-id="1976e-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="1976e-131">Wenn diese Eigenschaft für einen Speicher festgelegt ist, der Outlook 2003 SP 1 verwendet, wird von Outlook die Größe der einzelnen angegebenen Ordner auf dem Server und dem lokalen Laufwerk abgefragt.</span><span class="sxs-lookup"><span data-stu-id="1976e-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="1976e-132">Zum Abfragen der Ordnergröße auf dem Server öffnet Outlook einen Ordner im Speicher mit [IMsgStore::OpenEntry,](imsgstore-openentry.md)übergeben das Flag **MAPI_NO_CACHE**, und fragt dann nach PR_MESSAGE_SIZE_EXTENDED **.**</span><span class="sxs-lookup"><span data-stu-id="1976e-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="1976e-133">Der Speicheranbieter sollte dann die Ordnergröße auf dem Server zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1976e-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="1976e-134">Um die Größe eines Ordners auf dem lokalen Laufwerk zu abfragen, öffnet Outlook den Ordner ohne **MAPI_NO_CACHE** Flag.</span><span class="sxs-lookup"><span data-stu-id="1976e-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="1976e-135">Anschließend werden Abfragen für **PR_MESSAGE_SIZE_EXTENDED**; Der Speicheranbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1976e-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="1976e-136">Mit diesem Eigenschaftensatz können Anbieter, die Speicherinhalte mit einem Server synchronisieren, Im Dialogfeld Ordnergröße auf dem Server Outlook **Ordnergröße** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1976e-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="1976e-137">Benutzer können dann ihre aktuelle Serverspeichernutzung mit Serverkontingenten vergleichen.</span><span class="sxs-lookup"><span data-stu-id="1976e-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

