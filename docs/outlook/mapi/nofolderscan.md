---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793283"
---
# <a name="nofolderscan"></a><span data-ttu-id="961c3-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="961c3-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="961c3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="961c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="961c3-105">Gibt an, ob Microsoft Office Outlook-Ordner Kontakte in einem Speicher gescannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="961c3-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="961c3-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="961c3-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="961c3-107">Eingeblendet auf:</span><span class="sxs-lookup"><span data-stu-id="961c3-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="961c3-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt</span><span class="sxs-lookup"><span data-stu-id="961c3-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="961c3-109">Erstellt:</span><span class="sxs-lookup"><span data-stu-id="961c3-109">Created by:</span></span>  <br/> |<span data-ttu-id="961c3-110">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="961c3-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="961c3-111">Durch zugegriffen:</span><span class="sxs-lookup"><span data-stu-id="961c3-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="961c3-112">Outlook und andere clients</span><span class="sxs-lookup"><span data-stu-id="961c3-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="961c3-113">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="961c3-113">Property type:</span></span>  <br/> |<span data-ttu-id="961c3-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="961c3-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="961c3-115">Zugriffstyp:</span><span class="sxs-lookup"><span data-stu-id="961c3-115">Access type:</span></span>  <br/> |<span data-ttu-id="961c3-116">Nur-Lese- oder Lese-/Schreibzugriff, je nach Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="961c3-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="961c3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="961c3-117">Remarks</span></span>

<span data-ttu-id="961c3-118">Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="961c3-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="961c3-119">Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="961c3-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="961c3-120">[HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="961c3-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="961c3-121">Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="961c3-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="961c3-122">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="961c3-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="961c3-123">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="961c3-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="961c3-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="961c3-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="961c3-125">UlKind:</span><span class="sxs-lookup"><span data-stu-id="961c3-125">ulKind:</span></span>  <br/> |<span data-ttu-id="961c3-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="961c3-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="961c3-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="961c3-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="961c3-128">L "NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="961c3-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="961c3-129">Diese Eigenschaft bietet eine Möglichkeit für Anbieter, um Outlook anzugeben, nicht zum Scannen Kontakteordner im Speicher um eine leistungsbeeinträchtigung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="961c3-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="961c3-130">Es wird im Seriendruck-Vorgänge in denen Outlook überprüft das Vorhandensein und der Wert dieser Eigenschaft verwendet, bevor Sie mit der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="961c3-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="961c3-131">Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar gemacht bedeutet, dass Outlook den Ordner Kontakte für den Speicher gescannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="961c3-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="961c3-132">Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden die möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="961c3-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="961c3-133">Null (0): Outlook kann die Überprüfung ausführen.</span><span class="sxs-lookup"><span data-stu-id="961c3-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="961c3-134">Wert ungleich NULL: Outlook sollte Kontakteordner im Store nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="961c3-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

