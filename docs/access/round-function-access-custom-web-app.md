---
title: Round-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Gibt einen abgerundeten oder abgeschnittenen numerischen Wert auf die angegebene Länge oder Genauigkeit zurück.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307959"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="a22cb-103">Round-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="a22cb-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="a22cb-104">Gibt einen abgerundeten oder abgeschnittenen numerischen Wert auf die angegebene Länge oder Genauigkeit zurück.</span><span class="sxs-lookup"><span data-stu-id="a22cb-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a22cb-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="a22cb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a22cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a22cb-107">Syntax</span></span>

 <span data-ttu-id="a22cb-108">**Round** (*Anzahl*, *Genauigkeit* , [ *TruncateInsteadOfRound* ])</span><span class="sxs-lookup"><span data-stu-id="a22cb-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="a22cb-109">Die **Round** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="a22cb-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a22cb-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="a22cb-110">**Argument name**</span></span>|<span data-ttu-id="a22cb-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a22cb-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a22cb-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="a22cb-112">*Number*</span></span>  <br/> |<span data-ttu-id="a22cb-113">Ein numerischer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="a22cb-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="a22cb-114">*Genauigkeit*</span><span class="sxs-lookup"><span data-stu-id="a22cb-114">*Precision*</span></span>  <br/> |<span data-ttu-id="a22cb-115">Die Genauigkeit, mit der die *Zahl* gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a22cb-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="a22cb-116">Bei der *Genauigkeit* muss es sich um einen numerischen Ausdruck handeln.</span><span class="sxs-lookup"><span data-stu-id="a22cb-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="a22cb-117">Wenn die *Genauigkeit* eine positive Zahl ist, wird *Zahl* auf die Anzahl der durch length angegebenen Dezimalstellen gerundet.</span><span class="sxs-lookup"><span data-stu-id="a22cb-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="a22cb-118">Wenn die *Genauigkeit* eine negative Zahl ist, wird die *Zahl* auf der linken Seite des Dezimalkommas, wie durch length angegeben, gerundet.</span><span class="sxs-lookup"><span data-stu-id="a22cb-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="a22cb-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="a22cb-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="a22cb-120">Der Typ des auszuführenden Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a22cb-120">The type of operation to perform.</span></span> <span data-ttu-id="a22cb-121">Wenn der Wert nicht angegeben oder auf 0 festgelegt ist, wird *Zahl* gerundet.</span><span class="sxs-lookup"><span data-stu-id="a22cb-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="a22cb-122">Wenn ein anderer Wert als 0 angegeben wird, wird *Number* abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a22cb-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="a22cb-123">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a22cb-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a22cb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a22cb-124">Remarks</span></span>

 <span data-ttu-id="a22cb-125">**Round** gibt immer einen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a22cb-125">**Round** always returns a value.</span></span> <span data-ttu-id="a22cb-126">Wenn length negativ und größer als die Anzahl der Ziffern vor dem Dezimaltrennzeichen ist, gibt **Round** den Wert 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="a22cb-126">If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

