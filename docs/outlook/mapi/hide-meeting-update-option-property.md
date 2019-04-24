---
title: Option-Eigenschaft für Besprechungs Update ausblenden
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299510"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="56899-103">Option-Eigenschaft für Besprechungs Update ausblenden</span><span class="sxs-lookup"><span data-stu-id="56899-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="56899-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56899-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56899-105">Blendet die Option zum Senden von Besprechungs Updates an nur hinzugefügte oder gelöschte Teilnehmer aus.</span><span class="sxs-lookup"><span data-stu-id="56899-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="56899-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="56899-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56899-107">Verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="56899-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="56899-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Objekt</span><span class="sxs-lookup"><span data-stu-id="56899-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="56899-109">Erstellt von:</span><span class="sxs-lookup"><span data-stu-id="56899-109">Created by:</span></span>  <br/> |<span data-ttu-id="56899-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="56899-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="56899-111">Zugriff durch:</span><span class="sxs-lookup"><span data-stu-id="56899-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="56899-112">Outlook und andere Clients</span><span class="sxs-lookup"><span data-stu-id="56899-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="56899-113">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="56899-113">Property type:</span></span>  <br/> |<span data-ttu-id="56899-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="56899-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="56899-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="56899-115">Access type:</span></span>  <br/> |<span data-ttu-id="56899-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="56899-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56899-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56899-117">Remarks</span></span>

<span data-ttu-id="56899-118">Um eine der Store-Funktionen bereitzustellen, muss der Informationsspeicher Anbieter [IMAPIProp: IUnknown](imapipropiunknown.md) implementieren und ein gültiges Property-Tag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="56899-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="56899-119">Wenn das Property-Tag für eine dieser Eigenschaften an [IMAPIProp::](imapiprop-getprops.md)GetProps übergeben wird, muss der Informationsspeicher Anbieter auch den richtigen Eigenschaftswert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="56899-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="56899-120">Speicheranbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="56899-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="56899-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Property-Tag abzurufen, und dann dieses Property-Tag in [IMAPIProp::](imapiprop-getprops.md) GetProps angeben, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="56899-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="56899-122">Geben Sie beim Aufrufen von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, auf die durch den Eingabeparameter _lppPropNames_verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="56899-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56899-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="56899-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="56899-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="56899-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="56899-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="56899-125">ulKind:</span></span>  <br/> |<span data-ttu-id="56899-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="56899-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="56899-127">Art. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="56899-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="56899-128">L "urn: Schemas-Microsoft-com: Office: Outlook # allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="56899-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="56899-129">Ein Informationsspeicher Anbieter, der einen Server zum Senden von Besprechungs Updates verwendet, kann das Dialogfeld **Update an Teilnehmer senden** ändern.</span><span class="sxs-lookup"><span data-stu-id="56899-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="56899-130">Diese Funktion ist nützlich, da der Server nicht weiß, welche Teilnehmer seit der anfänglichen Besprechungsanfrage vom Benutzer hinzugefügt oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="56899-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="56899-131">Wenn diese Eigenschaft auf **true**festgelegt ist, wird die Option **nur Update an hinzugefügte oder gelöschte Teilnehmer senden** nicht im Dialogfeld an **Teilnehmer senden** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56899-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="56899-132">Diese Eigenschaft wird ignoriert, wenn die Version von Outlook älter als Microsoft Office Outlook 2003 Service Pack 1 ist, oder wenn der Wert **false**ist.</span><span class="sxs-lookup"><span data-stu-id="56899-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

