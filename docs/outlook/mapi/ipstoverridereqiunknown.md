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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6ee4524d08e334df858c2f035f1b21bd2b0a1c8b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792806"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="2d093-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d093-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="2d093-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d093-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d093-105">Greift auf Ressourcen in einen Anbieter für Persönliche Ordner-Datei (PST) anmelden.</span><span class="sxs-lookup"><span data-stu-id="2d093-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d093-106">Erbt:</span><span class="sxs-lookup"><span data-stu-id="2d093-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="2d093-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d093-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="2d093-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2d093-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2d093-109">PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="2d093-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="2d093-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2d093-110">Called by:</span></span>  <br/> |<span data-ttu-id="2d093-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="2d093-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="2d093-112">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2d093-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2d093-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="2d093-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2d093-114">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2d093-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2d093-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="2d093-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="2d093-116">Initiiert das Aufheben der Sperre Verfahren für den persönlichen Ordner (PST).</span><span class="sxs-lookup"><span data-stu-id="2d093-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d093-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d093-117">Remarks</span></span>

<span data-ttu-id="2d093-118">Die PST-Datei überschreiben Handler Schnittstellenbezeichner möglicherweise nicht in der herunterladbaren Headerdatei definiert werden derzeit, in diesem Fall müssen Sie finden sie im Thema [MAPI-Konstanten](mapi-constants.md) und können kopieren und fügen sie dem Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d093-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="2d093-119">Verwenden Sie das DEFINE_GUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, deren Werte symbolische Namen global eindeutigen Bezeichner (GUID) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2d093-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="2d093-120">Weitere Informationen finden Sie unter [ein PST Außerkraftsetzung Handler für die Umgehung die PSTDisableGrow Richtlinie in Outlook 2007 implementiert wird](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="2d093-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d093-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d093-121">See also</span></span>



[<span data-ttu-id="2d093-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d093-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

