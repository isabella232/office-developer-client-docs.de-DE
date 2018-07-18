---
title: LOCALFORMULAEXISTS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Gibt an, ob die referenzierte Zelle eine lokale Formel enthält.
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797368"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="dfc44-103">LOCALFORMULAEXISTS Function</span><span class="sxs-lookup"><span data-stu-id="dfc44-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="dfc44-104">Gibt an, ob die referenzierte Zelle eine lokale Formel enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc44-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dfc44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfc44-105">Syntax</span></span>

<span data-ttu-id="dfc44-106">LOCALFORMULAEXISTS (** *Cellref* **)</span><span class="sxs-lookup"><span data-stu-id="dfc44-106">LOCALFORMULAEXISTS (** *cellref* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dfc44-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfc44-107">Parameters</span></span>

|<span data-ttu-id="dfc44-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dfc44-108">**Name**</span></span>|<span data-ttu-id="dfc44-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="dfc44-109">**Required/Optional**</span></span>|<span data-ttu-id="dfc44-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="dfc44-110">**Data Type**</span></span>|<span data-ttu-id="dfc44-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dfc44-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dfc44-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="dfc44-112">_cellref_</span></span> <br/> |<span data-ttu-id="dfc44-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dfc44-113">Required</span></span>  <br/> |<span data-ttu-id="dfc44-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dfc44-114">**String**</span></span> <br/> | <span data-ttu-id="dfc44-115">Die Zelle, die auf das Vorhandensein einer Formel überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfc44-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dfc44-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dfc44-116">Return value</span></span>

<span data-ttu-id="dfc44-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="dfc44-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfc44-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfc44-118">Remarks</span></span>

<span data-ttu-id="dfc44-119">Die LOCALFORMULAEXISTS-Funktion gibt 1 zurück, wenn die Zelle eine Formel enthält; wenn keine Formel vorhanden ist oder wenn die Formel übernommen wurde, wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dfc44-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

