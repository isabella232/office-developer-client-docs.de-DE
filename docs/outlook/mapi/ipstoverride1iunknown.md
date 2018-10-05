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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382547"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="2e7fd-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e7fd-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="2e7fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e7fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e7fd-105">Ermöglicht einen Anbieter für Persönliche Ordner-Datei (PST) anmelden die PSTDisableGrow Richtlinie außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="2e7fd-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e7fd-106">Erbt:</span><span class="sxs-lookup"><span data-stu-id="2e7fd-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="2e7fd-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e7fd-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="2e7fd-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2e7fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e7fd-109">PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="2e7fd-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="2e7fd-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2e7fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="2e7fd-111">Client</span><span class="sxs-lookup"><span data-stu-id="2e7fd-111">Client</span></span>  <br/> |
|<span data-ttu-id="2e7fd-112">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2e7fd-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2e7fd-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="2e7fd-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2e7fd-114">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2e7fd-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2e7fd-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="2e7fd-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="2e7fd-116">Ruft die Liste von Einträgen für den persönlichen Ordner (PST) Datei ab.</span><span class="sxs-lookup"><span data-stu-id="2e7fd-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="2e7fd-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="2e7fd-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="2e7fd-118">Registriert Persönliche Ordner-Dateien für die automatische Entsperren Weitere Anrufe an HrTrustedPSTOverrideHandlerCallback zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2e7fd-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="2e7fd-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="2e7fd-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="2e7fd-120">Hebt die Sperre für das Wachstum der Persönliche Ordner-Datei.</span><span class="sxs-lookup"><span data-stu-id="2e7fd-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e7fd-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e7fd-121">Remarks</span></span>

<span data-ttu-id="2e7fd-122">Die PST-Datei überschreiben Handler Schnittstellenbezeichner möglicherweise nicht in der herunterladbaren Headerdatei definiert werden derzeit, in diesem Fall müssen Sie finden sie im Thema [MAPI-Konstanten](mapi-constants.md) und können kopieren und fügen sie dem Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e7fd-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="2e7fd-123">Verwenden Sie das DEFINE_GUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, deren Werte symbolische Namen global eindeutigen Bezeichner (GUID) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2e7fd-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="2e7fd-124">Weitere Informationen finden Sie unter [ein PST Außerkraftsetzung Handler für die Umgehung die PSTDisableGrow Richtlinie in Outlook 2007 implementiert wird](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="2e7fd-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2e7fd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e7fd-125">See also</span></span>



[<span data-ttu-id="2e7fd-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e7fd-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

