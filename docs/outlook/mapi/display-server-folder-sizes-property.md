---
title: Display Server Folder sizes-Eigenschaft
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
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337079"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="68769-103">Display Server Folder sizes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68769-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="68769-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68769-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68769-105">Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook- **Ordnergröße** an.</span><span class="sxs-lookup"><span data-stu-id="68769-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="68769-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="68769-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68769-107">Verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="68769-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="68769-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="68769-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="68769-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="68769-109">Created by:</span></span>  <br/> |<span data-ttu-id="68769-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="68769-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="68769-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="68769-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="68769-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="68769-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="68769-113">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="68769-113">Property type:</span></span>  <br/> |<span data-ttu-id="68769-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="68769-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="68769-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="68769-115">Access type:</span></span>  <br/> |<span data-ttu-id="68769-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68769-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68769-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68769-117">Remarks</span></span>

<span data-ttu-id="68769-118">Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="68769-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="68769-119">Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68769-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="68769-120">Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="68769-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="68769-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="68769-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="68769-122">Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="68769-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68769-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="68769-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="68769-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="68769-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="68769-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="68769-125">ulKind:</span></span>  <br/> |<span data-ttu-id="68769-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="68769-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="68769-127">Art. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="68769-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="68769-128">L "urn: Schemas-Microsoft-com: Office: Outlook # serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="68769-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="68769-129">Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68769-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="68769-130">Wenn die Version von Outlook älter als Outlook 2003 SP 1 ist oder wenn der Wert **false**ist, zeigt Outlook nur die Größe der Ordner im lokalen Speicher an.</span><span class="sxs-lookup"><span data-stu-id="68769-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="68769-131">Wenn diese Eigenschaft in einem Speicher festgelegt ist, der Outlook 2003 SP 1 verwendet, fragt Outlook die Größe jedes angegebenen Ordners auf dem Server und dem lokalen Laufwerk ab.</span><span class="sxs-lookup"><span data-stu-id="68769-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="68769-132">Um die Ordnergröße auf dem Server abzufragen, öffnet Outlook einen Ordner im Store mit [IMsgStore:: OpenEntry](imsgstore-openentry.md), übergibt das Flag **MAPI_NO_CACHE**und fragt dann nach **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="68769-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="68769-133">Der Informationsspeicher Anbieter sollte dann die Größe des Ordners auf dem Server zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68769-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="68769-134">Wenn Sie die Größe eines Ordners auf dem lokalen Laufwerk Abfragen möchten, wird der Ordner ohne das **MAPI_NO_CACHE** -Flag geöffnet.</span><span class="sxs-lookup"><span data-stu-id="68769-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="68769-135">Dann fragt Sie nach **PR_MESSAGE_SIZE_EXTENDED**; der Informationsspeicher Anbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68769-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="68769-136">Mit dieser Eigenschaft können Speicheranbieter, die Speicherinhalte mit einem Server synchronisieren, Daten auf dem Server im Dialogfeld Outlook- **Ordner** Größe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="68769-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="68769-137">Benutzer können dann Ihre aktuelle Server Speicherauslastung mit Server Kontingenten vergleichen.</span><span class="sxs-lookup"><span data-stu-id="68769-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

