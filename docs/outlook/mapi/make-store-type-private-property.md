---
title: Make Store Type Private Property
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
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428543"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="a5f93-103">Make Store Type Private Property</span><span class="sxs-lookup"><span data-stu-id="a5f93-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="a5f93-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5f93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5f93-105">Behandelt einen sekundären Speicher als privat.</span><span class="sxs-lookup"><span data-stu-id="a5f93-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a5f93-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a5f93-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5f93-107">Verfügbar gemacht für:</span><span class="sxs-lookup"><span data-stu-id="a5f93-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="a5f93-108">[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="a5f93-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="a5f93-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="a5f93-109">Created by:</span></span>  <br/> |<span data-ttu-id="a5f93-110">Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="a5f93-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="a5f93-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="a5f93-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="a5f93-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="a5f93-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="a5f93-113">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="a5f93-113">Property type:</span></span>  <br/> |<span data-ttu-id="a5f93-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a5f93-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a5f93-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="a5f93-115">Access type:</span></span>  <br/> |<span data-ttu-id="a5f93-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a5f93-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5f93-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5f93-117">Remarks</span></span>

<span data-ttu-id="a5f93-118">Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a5f93-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="a5f93-119">Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a5f93-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="a5f93-120">Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="a5f93-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="a5f93-121">Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5f93-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="a5f93-122">Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_</span><span class="sxs-lookup"><span data-stu-id="a5f93-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5f93-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="a5f93-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="a5f93-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a5f93-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="a5f93-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="a5f93-125">ulKind:</span></span>  <br/> |<span data-ttu-id="a5f93-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="a5f93-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="a5f93-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="a5f93-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="a5f93-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="a5f93-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="a5f93-129">Ein Speicheranbieter kann diese Eigenschaft verwenden, um Outlook als privat zu behandeln, wenn es sich um einen sekundären Speicher für einen Benutzer handelt.</span><span class="sxs-lookup"><span data-stu-id="a5f93-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="a5f93-130">Standardmäßig behandelt Outlook einen sekundären Speicher auf die gleiche Weise wie ein Stellvertretungsspeicher, und Elemente im sekundären Speicher sind nur dann privat, wenn der Benutzer sie speziell als privat kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a5f93-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="a5f93-131">Wenn diese Eigenschaft **true ist,** werden elemente, die aus einem sekundären Speicher gelöscht wurden, in den Ordner **Gelöschte** Elemente im primären Speicher verschoben.</span><span class="sxs-lookup"><span data-stu-id="a5f93-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="a5f93-132">Als privat markierte Elemente werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5f93-132">Items marked private are not displayed.</span></span> <span data-ttu-id="a5f93-133">Entwürfe werden im Ordner Entwürfe im primären Speicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a5f93-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="a5f93-134">Diese Eigenschaft wird ignoriert, wenn die Version von Outlook vor Microsoft Office Outlook 2003 Service Pack 1 liegt oder wenn ihr Wert **false ist.**</span><span class="sxs-lookup"><span data-stu-id="a5f93-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

