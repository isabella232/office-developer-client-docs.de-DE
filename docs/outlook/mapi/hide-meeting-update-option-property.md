---
title: Option "Besprechungsupdate ausblenden"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412100"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="c81fe-103">Option "Besprechungsupdate ausblenden"</span><span class="sxs-lookup"><span data-stu-id="c81fe-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="c81fe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c81fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c81fe-105">Blendet die Option zum Senden von Besprechungsupdates nur an hinzugefügte oder gelöschte Teilnehmer aus.</span><span class="sxs-lookup"><span data-stu-id="c81fe-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c81fe-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c81fe-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c81fe-107">Verfügbar gemacht für:</span><span class="sxs-lookup"><span data-stu-id="c81fe-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="c81fe-108">[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c81fe-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="c81fe-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="c81fe-109">Created by:</span></span>  <br/> |<span data-ttu-id="c81fe-110">Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="c81fe-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="c81fe-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="c81fe-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="c81fe-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="c81fe-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="c81fe-113">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="c81fe-113">Property type:</span></span>  <br/> |<span data-ttu-id="c81fe-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c81fe-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c81fe-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="c81fe-115">Access type:</span></span>  <br/> |<span data-ttu-id="c81fe-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c81fe-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c81fe-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c81fe-117">Remarks</span></span>

<span data-ttu-id="c81fe-118">Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c81fe-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="c81fe-119">Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c81fe-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="c81fe-120">Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="c81fe-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="c81fe-121">Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c81fe-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="c81fe-122">Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_</span><span class="sxs-lookup"><span data-stu-id="c81fe-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c81fe-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="c81fe-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="c81fe-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="c81fe-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="c81fe-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="c81fe-125">ulKind:</span></span>  <br/> |<span data-ttu-id="c81fe-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="c81fe-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="c81fe-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="c81fe-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="c81fe-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="c81fe-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="c81fe-129">Ein Speicheranbieter, der einen Server zum Senden von Besprechungsupdates verwendet, kann das Dialogfeld **Update an Teilnehmer** senden ändern.</span><span class="sxs-lookup"><span data-stu-id="c81fe-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="c81fe-130">Diese Funktionalität ist nützlich, da der Server beim Senden eines Besprechungsupdates nicht weiß, welche Teilnehmer seit der ersten Besprechungsanfrage vom Benutzer hinzugefügt oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="c81fe-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="c81fe-131">Wenn diese Eigenschaft **true** ist, wird die Option Update nur für hinzugefügte oder gelöschte Teilnehmer senden nicht im Dialogfeld Update an **Teilnehmer** senden angezeigt. </span><span class="sxs-lookup"><span data-stu-id="c81fe-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="c81fe-132">Diese Eigenschaft wird ignoriert, wenn die Version von Outlook vor Microsoft Office Outlook 2003 Service Pack 1 liegt oder wenn ihr Wert **false ist.**</span><span class="sxs-lookup"><span data-stu-id="c81fe-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

