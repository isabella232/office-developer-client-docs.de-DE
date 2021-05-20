---
title: Konstanten (Frei/Gebucht-API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Dieses Thema enthält Konstantendefinitionen, Klassenbezeichner und Schnittstellenbezeichner für die Frei/Gebucht-API.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431533"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="e74b3-103">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="e74b3-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="e74b3-104">Dieses Thema enthält Konstantendefinitionen, Klassenbezeichner und Schnittstellenbezeichner für die Frei/Gebucht-API.</span><span class="sxs-lookup"><span data-stu-id="e74b3-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="e74b3-105">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e74b3-105">Constants</span></span>

|<span data-ttu-id="e74b3-106">**Konstante**</span><span class="sxs-lookup"><span data-stu-id="e74b3-106">**Constant**</span></span>|<span data-ttu-id="e74b3-107">**Definition**</span><span class="sxs-lookup"><span data-stu-id="e74b3-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e74b3-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="e74b3-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="e74b3-109">*Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei winerror.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="e74b3-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="e74b3-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e74b3-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="e74b3-111">*Wie in der Windows sdk-Headerdatei winerror.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="e74b3-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="e74b3-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e74b3-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="e74b3-113">*Wie in der Windows sdk-Headerdatei winerror.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="e74b3-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="e74b3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e74b3-114">S_OK</span></span>  <br/> | <span data-ttu-id="e74b3-115">*Wie in der Windows sdk-Headerdatei winerror.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="e74b3-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="e74b3-116">Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="e74b3-116">Interface identifiers</span></span>

<span data-ttu-id="e74b3-117">Gehen Sie für die folgenden Schnittstellenbezeichner davon aus, dass das DEFINE_GUID-Makro, das in der Windows-SDK-Headerdatei guiddef.h definiert ist, den symbolischen NAMEN der GUID seinem Wert zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e74b3-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="e74b3-118">{00067064-0000-0000-C000-0000000000046}</span><span class="sxs-lookup"><span data-stu-id="e74b3-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="e74b3-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="e74b3-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="e74b3-120">{00067066-0000-0000-C000-0000000000046}</span><span class="sxs-lookup"><span data-stu-id="e74b3-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="e74b3-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="e74b3-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="e74b3-122">{00067067-0000-0000-C000-0000000000046}</span><span class="sxs-lookup"><span data-stu-id="e74b3-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="e74b3-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="e74b3-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

