---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356980"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="0d84a-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d84a-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="0d84a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d84a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d84a-105">Accesses resources of a Personal Folders file (PST) store provider.</span><span class="sxs-lookup"><span data-stu-id="0d84a-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d84a-106">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="0d84a-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="0d84a-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d84a-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="0d84a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0d84a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d84a-109">Anbieter für den PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="0d84a-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="0d84a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0d84a-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d84a-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="0d84a-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="0d84a-112">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="0d84a-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0d84a-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="0d84a-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0d84a-114">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0d84a-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0d84a-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="0d84a-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="0d84a-116">Initiiert die Entsperrprozedur für eine Datei mit persönlichen Ordnern (PST).</span><span class="sxs-lookup"><span data-stu-id="0d84a-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d84a-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d84a-117">Remarks</span></span>

<span data-ttu-id="0d84a-118">Die Pst Override Handler Interface Identifiers sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall finden Sie sie im Thema [MAPI-Konstanten](mapi-constants.md) und können sie kopieren und ihrem Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d84a-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="0d84a-119">Verwenden Sie das DEFINE_GUID, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definiert ist, um ihren Werten symbolische Namen (Globally Unique Identifier, GUID) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0d84a-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="0d84a-120">Weitere Informationen finden Sie unter Implementieren eines PST-Außerkraftsetzungshandlers zum Umgehen der [PSTDisableGrow-Richtlinie in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="0d84a-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d84a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d84a-121">See also</span></span>



[<span data-ttu-id="0d84a-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d84a-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

