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
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="6a873-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a873-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="6a873-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a873-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a873-105">Greift auf Ressourcen eines PST-Speicheranbieters (Personal Folders File) zu.</span><span class="sxs-lookup"><span data-stu-id="6a873-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a873-106">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="6a873-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="6a873-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a873-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="6a873-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6a873-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a873-109">PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="6a873-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="6a873-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6a873-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a873-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6a873-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="6a873-112">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6a873-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6a873-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="6a873-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6a873-114">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6a873-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6a873-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="6a873-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="6a873-116">Initiiert die entsperrungs Prozedur für eine persönliche Ordner-Datei (PST).</span><span class="sxs-lookup"><span data-stu-id="6a873-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a873-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a873-117">Remarks</span></span>

<span data-ttu-id="6a873-118">Die Schnittstellenbezeichner für den PST-Außerkraftsetzungs Handler sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall werden Sie Sie im Thema [MAPI-Konstanten](mapi-constants.md) finden, und Sie können Sie kopieren und Ihrem Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6a873-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="6a873-119">Verwenden Sie das DEFINE_GUID-Makro, das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef. h definiert ist, um GUID-symbolische Namen (Globally Unique Identifier) mit ihren Werten zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6a873-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="6a873-120">Weitere Informationen finden Sie unter [How to implement a PST override Handler to Bypass the PSTDisableGrow Policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="6a873-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a873-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a873-121">See also</span></span>



[<span data-ttu-id="6a873-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a873-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

