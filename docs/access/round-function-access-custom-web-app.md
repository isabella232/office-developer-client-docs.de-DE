---
title: Round-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen numerischen Wert( gerundet oder abgeschnitten) auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413745"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="d5d91-103">Round-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="d5d91-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="d5d91-104">Gibt einen numerischen Wert( gerundet oder abgeschnitten) auf die angegebene Länge oder Genauigkeit zurück.</span><span class="sxs-lookup"><span data-stu-id="d5d91-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d5d91-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="d5d91-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d5d91-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5d91-107">Syntax</span></span>

 <span data-ttu-id="d5d91-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span><span class="sxs-lookup"><span data-stu-id="d5d91-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="d5d91-109">Die **Round-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d5d91-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d5d91-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d5d91-110">**Argument name**</span></span>|<span data-ttu-id="d5d91-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5d91-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d5d91-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="d5d91-112">*Number*</span></span>  <br/> |<span data-ttu-id="d5d91-113">Ein numerischer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="d5d91-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="d5d91-114">*Genauigkeit*</span><span class="sxs-lookup"><span data-stu-id="d5d91-114">*Precision*</span></span>  <br/> |<span data-ttu-id="d5d91-115">Die Genauigkeit, auf die  *Number*  gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5d91-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="d5d91-116">*Genauigkeit*  muss ein numerischer Ausdruck sein.</span><span class="sxs-lookup"><span data-stu-id="d5d91-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="d5d91-117">Wenn  *Precision*  eine positive Zahl ist, wird  *Number*  auf die Anzahl der dezimalen Positionen gerundet, die durch die Länge angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d5d91-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="d5d91-118">Wenn  *Precision*  eine negative Zahl ist, wird  *Number*  auf der linken Seite des Dezimalkomma gerundet, wie durch die Länge angegeben.</span><span class="sxs-lookup"><span data-stu-id="d5d91-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="d5d91-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="d5d91-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="d5d91-120">Der Typ des durchzuführende Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d5d91-120">The type of operation to perform.</span></span> <span data-ttu-id="d5d91-121">Wenn sie nicht angegeben oder auf 0 festgelegt ist,  *wird Number*  gerundet.</span><span class="sxs-lookup"><span data-stu-id="d5d91-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="d5d91-122">Wenn ein anderer Wert als 0 angegeben wird, wird  *Number*  abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="d5d91-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="d5d91-123">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="d5d91-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5d91-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5d91-124">Remarks</span></span>

 <span data-ttu-id="d5d91-125">**Round** gibt immer einen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5d91-125">**Round** always returns a value.</span></span> <span data-ttu-id="d5d91-126">Wenn die Länge negativ und größer als die Anzahl der Ziffern vor dem Dezimalkomma ist, gibt **Round** 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="d5d91-126">If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

