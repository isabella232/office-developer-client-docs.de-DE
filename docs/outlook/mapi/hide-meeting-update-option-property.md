---
title: Eigenschaft zum Ausblenden der Besprechungsaktualisierungsoption
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
ms.openlocfilehash: 65255e14fd849d730e92bd86027642eef2c687bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584975"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="0c2cd-103">Eigenschaft zum Ausblenden der Besprechungsaktualisierungsoption</span><span class="sxs-lookup"><span data-stu-id="0c2cd-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="0c2cd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c2cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c2cd-105">Blendet die Option zum besprechungsaktualisierungen auf nur hinzugefügte oder gelöschte Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0c2cd-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="0c2cd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c2cd-107">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="0c2cd-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt</span><span class="sxs-lookup"><span data-stu-id="0c2cd-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="0c2cd-109">Erstellt:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-109">Created by:</span></span>  <br/> |<span data-ttu-id="0c2cd-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="0c2cd-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="0c2cd-111">Durch zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="0c2cd-112">Outlook und andere clients</span><span class="sxs-lookup"><span data-stu-id="0c2cd-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="0c2cd-113">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-113">Property type:</span></span>  <br/> |<span data-ttu-id="0c2cd-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0c2cd-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0c2cd-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-115">Access type:</span></span>  <br/> |<span data-ttu-id="0c2cd-116">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="0c2cd-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c2cd-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0c2cd-117">Remarks</span></span>

<span data-ttu-id="0c2cd-118">Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="0c2cd-119">Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="0c2cd-120">[HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="0c2cd-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="0c2cd-122">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c2cd-123">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="0c2cd-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="0c2cd-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="0c2cd-125">UlKind:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-125">ulKind:</span></span>  <br/> |<span data-ttu-id="0c2cd-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="0c2cd-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="0c2cd-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="0c2cd-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="0c2cd-128">L "Urn: Schemas-Microsoft-Com:office:outlook #allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="0c2cd-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="0c2cd-129">Ein Anbieter anmelden, der einen Server verwendet, um die Besprechung aktualisiert senden kann das Dialogfeld **Aktualisierung an Teilnehmer senden** ändern.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="0c2cd-130">Diese Funktion ist hilfreich, da bei der Server eine besprechungsaktualisierung sendet, der Server nicht bekannt ist, welche Teilnehmer hinzugefügt oder vom Benutzer gegenüber der ursprünglichen Besprechungsanfrage gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="0c2cd-131">Wenn diese Eigenschaft auf **true**festgelegt ist, wird die Option **Update nur für hinzugefügten oder gelöschten Teilnehmer senden** nicht im Dialogfeld **Aktualisierung an Teilnehmer senden** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="0c2cd-132">Diese Eigenschaft wird ignoriert, wenn die Version von Outlook einer älteren Version als Microsoft Office Outlook 2003 Service Pack 1 ist oder wenn der Wert **false**lautet.</span><span class="sxs-lookup"><span data-stu-id="0c2cd-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

