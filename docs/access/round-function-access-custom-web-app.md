---
title: Round-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen numerischen Wert, entweder gerundet oder abgeschnitten werden, auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790358"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="ba6a4-103">Round-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="ba6a4-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="ba6a4-104">Gibt einen numerischen Wert, entweder gerundet oder abgeschnitten werden, auf die angegebene Länge oder Genauigkeit zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ba6a4-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ba6a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba6a4-107">Syntax</span></span>

 <span data-ttu-id="ba6a4-108">**Round** (*Anzahl*, *Precision* , [ *TruncateInsteadOfRound* ])</span><span class="sxs-lookup"><span data-stu-id="ba6a4-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="ba6a4-109">Die **Round** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ba6a4-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="ba6a4-110">**Argument name**</span></span>|<span data-ttu-id="ba6a4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ba6a4-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ba6a4-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="ba6a4-112">*Number*</span></span>  <br/> |<span data-ttu-id="ba6a4-113">Ein numerischer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="ba6a4-114">*Mit doppelter Genauigkeit*</span><span class="sxs-lookup"><span data-stu-id="ba6a4-114">*Precision*</span></span>  <br/> |<span data-ttu-id="ba6a4-115">Die Genauigkeit an die *Zahl* gerundet werden ist.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="ba6a4-116">*Genauigkeit* muss es sich um einen numerischen Ausdruck sein.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="ba6a4-117">Wenn *Genauigkeit* eine positive Zahl ist, wird die Anzahl der angegebenen Länge decimal Positionen *Zahl* gerundet.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="ba6a4-118">Wenn *Genauigkeit* eine negative Zahl ist, wird auf der linken Seite neben dem Dezimalkomma gemäß Länge *Zahl* gerundet.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="ba6a4-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="ba6a4-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="ba6a4-120">Der Typ der auszuführenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-120">The type of operation to perform.</span></span> <span data-ttu-id="ba6a4-121">Wenn nicht angegeben oder auf 0 festlegen, wird die *Zahl* gerundet.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="ba6a4-122">Wenn ein anderer Wert als 0 angegeben wird, wird die *Zahl* gekürzt.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="ba6a4-123">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba6a4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba6a4-124">Remarks</span></span>

 <span data-ttu-id="ba6a4-125">**Round** gibt immer einen Wert.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-125">**Round** always returns a value.</span></span> <span data-ttu-id="ba6a4-126">Ist Length negativ und größer als die Anzahl der Stellen vor dem Dezimalkomma, **Round** gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6a4-126">If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

