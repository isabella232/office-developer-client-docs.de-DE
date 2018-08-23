---
title: Eingenschaft zum Markieren des Store-Typs als privat
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2d927b00391725d8804e41b66b1ec8c384f98e7c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568833"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="a856e-103">Eingenschaft zum Markieren des Store-Typs als privat</span><span class="sxs-lookup"><span data-stu-id="a856e-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="a856e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a856e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a856e-105">Wird einen sekundären Speicher als privat behandelt.</span><span class="sxs-lookup"><span data-stu-id="a856e-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a856e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a856e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a856e-107">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="a856e-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="a856e-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt</span><span class="sxs-lookup"><span data-stu-id="a856e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="a856e-109">Erstellt:</span><span class="sxs-lookup"><span data-stu-id="a856e-109">Created by:</span></span>  <br/> |<span data-ttu-id="a856e-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="a856e-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="a856e-111">Durch zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="a856e-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="a856e-112">Outlook und andere clients</span><span class="sxs-lookup"><span data-stu-id="a856e-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="a856e-113">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="a856e-113">Property type:</span></span>  <br/> |<span data-ttu-id="a856e-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a856e-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a856e-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="a856e-115">Access type:</span></span>  <br/> |<span data-ttu-id="a856e-116">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="a856e-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a856e-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a856e-117">Remarks</span></span>

<span data-ttu-id="a856e-118">Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a856e-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="a856e-119">Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a856e-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="a856e-120">[HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a856e-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="a856e-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="a856e-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="a856e-122">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="a856e-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a856e-123">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="a856e-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="a856e-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a856e-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="a856e-125">UlKind:</span><span class="sxs-lookup"><span data-stu-id="a856e-125">ulKind:</span></span>  <br/> |<span data-ttu-id="a856e-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="a856e-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="a856e-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="a856e-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="a856e-128">L "Urn: Schemas-Microsoft-Com:office:outlook #storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="a856e-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="a856e-129">Ein Anbieter kann diese Eigenschaft verwenden, damit Outlook als privat behandelt, wenn es sich um einen sekundären Speicher für einen Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="a856e-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="a856e-130">In der Standardeinstellung Outlook einen sekundären Speicher behandelt die gleiche Weise wie ein Delegatspeicher und Elemente in den sekundären Speicher private nur, wenn der Benutzer diese speziell als privat markiert sind.</span><span class="sxs-lookup"><span data-stu-id="a856e-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="a856e-131">Wenn diese Eigenschaft auf **true**festgelegt ist, werden in den Ordner **Gelöschte Objekte** in den primären Speicher in einem sekundären Speicher gelöschte Elemente verschoben.</span><span class="sxs-lookup"><span data-stu-id="a856e-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="a856e-132">Als privat gekennzeichnete Elemente werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a856e-132">Items marked private are not displayed.</span></span> <span data-ttu-id="a856e-133">Entwürfe werden im Ordner "Entwürfe" in den primären Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a856e-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="a856e-134">Diese Eigenschaft wird ignoriert, wenn die Version von Outlook einer älteren Version als Microsoft Office Outlook 2003 Service Pack 1 ist oder wenn der Wert **false**lautet.</span><span class="sxs-lookup"><span data-stu-id="a856e-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

