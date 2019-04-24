---
title: Speichertyp als private Eigenschaft festlegen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298467"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="5ad0e-103">Speichertyp als private Eigenschaft festlegen</span><span class="sxs-lookup"><span data-stu-id="5ad0e-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="5ad0e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ad0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ad0e-105">Behandelt einen sekundären Speicher als privat.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5ad0e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="5ad0e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ad0e-107">Verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="5ad0e-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="5ad0e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="5ad0e-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-109">Created by:</span></span>  <br/> |<span data-ttu-id="5ad0e-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="5ad0e-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="5ad0e-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="5ad0e-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="5ad0e-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="5ad0e-113">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-113">Property type:</span></span>  <br/> |<span data-ttu-id="5ad0e-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ad0e-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ad0e-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-115">Access type:</span></span>  <br/> |<span data-ttu-id="5ad0e-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5ad0e-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ad0e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ad0e-117">Remarks</span></span>

<span data-ttu-id="5ad0e-118">Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="5ad0e-119">Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="5ad0e-120">Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="5ad0e-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="5ad0e-122">Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ad0e-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="5ad0e-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="5ad0e-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="5ad0e-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-125">ulKind:</span></span>  <br/> |<span data-ttu-id="5ad0e-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5ad0e-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="5ad0e-127">Art. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="5ad0e-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="5ad0e-128">L "urn: Schemas-Microsoft-com: Office: Outlook # storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="5ad0e-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="5ad0e-129">Ein Informationsspeicher Anbieter kann diese Eigenschaft verwenden, damit Outlook Sie als private behandelt, wenn es sich um einen sekundären Speicher für einen Benutzer handelt.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="5ad0e-130">Standardmäßig behandelt Outlook einen sekundären Speicher auf dieselbe Weise wie ein Stellvertreter Speicher, und Elemente im sekundären Speicher sind nur dann privat, wenn der Benutzer Sie ausdrücklich als privat kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="5ad0e-131">Wenn diese Eigenschaft auf **true**festgelegt ist, werden aus einem sekundären Speicher gelöschte Elemente in den Ordner **Gelöschte Elemente** im primären Speicher verschoben.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="5ad0e-132">Als privat gekennzeichnete Elemente werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-132">Items marked private are not displayed.</span></span> <span data-ttu-id="5ad0e-133">Entwürfe werden im Ordner "Entwürfe" im primären Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="5ad0e-134">Diese Eigenschaft wird ignoriert, wenn die Version von Outlook älter als Microsoft Office Outlook 2003 Service Pack 1 ist, oder wenn der Wert **false**ist.</span><span class="sxs-lookup"><span data-stu-id="5ad0e-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

