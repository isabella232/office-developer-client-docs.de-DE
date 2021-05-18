---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315498"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="97e8f-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97e8f-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="97e8f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97e8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97e8f-105">Ermöglicht einem Anbieter für den Informationsspeicher für persönliche Ordner (PST) das Außerkraft setzen der PSTDisableGrow-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="97e8f-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97e8f-106">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="97e8f-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="97e8f-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="97e8f-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="97e8f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="97e8f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="97e8f-109">Anbieter für den PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="97e8f-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="97e8f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="97e8f-110">Called by:</span></span>  <br/> |<span data-ttu-id="97e8f-111">Client</span><span class="sxs-lookup"><span data-stu-id="97e8f-111">Client</span></span>  <br/> |
|<span data-ttu-id="97e8f-112">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="97e8f-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="97e8f-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="97e8f-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="97e8f-114">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="97e8f-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="97e8f-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="97e8f-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="97e8f-116">Ruft die Liste der Registrierungen für die Datei Persönliche Ordner (PST) ab.</span><span class="sxs-lookup"><span data-stu-id="97e8f-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="97e8f-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="97e8f-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="97e8f-118">Registriert Persönliche Ordnerdateien für die automatische Entsperrung, um weitere Aufrufe von HrTrustedPSTOverrideHandlerCallback zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="97e8f-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="97e8f-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="97e8f-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="97e8f-120">Entsperrt eine Datei mit persönlichen Ordnern für das Wachstum.</span><span class="sxs-lookup"><span data-stu-id="97e8f-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97e8f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97e8f-121">Remarks</span></span>

<span data-ttu-id="97e8f-122">Die Pst Override Handler Interface Identifiers sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall finden Sie sie im Thema [MAPI-Konstanten](mapi-constants.md) und können sie kopieren und ihrem Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="97e8f-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="97e8f-123">Verwenden Sie das DEFINE_GUID, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definiert ist, um ihren Werten symbolische Namen (Globally Unique Identifier, GUID) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="97e8f-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="97e8f-124">Weitere Informationen finden Sie unter Implementieren eines PST-Außerkraftsetzungshandlers zum Umgehen der [PSTDisableGrow-Richtlinie in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="97e8f-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97e8f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97e8f-125">See also</span></span>



[<span data-ttu-id="97e8f-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97e8f-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

