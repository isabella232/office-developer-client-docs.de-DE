---
title: HASCATEGORY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433353"
---
# <a name="hascategory-function"></a><span data-ttu-id="c61e4-103">HASCATEGORY Function</span><span class="sxs-lookup"><span data-stu-id="c61e4-103">HASCATEGORY Function</span></span>

<span data-ttu-id="c61e4-104">Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.</span><span class="sxs-lookup"><span data-stu-id="c61e4-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="c61e4-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="c61e4-105">Version Information</span></span>

<span data-ttu-id="c61e4-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="c61e4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c61e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c61e4-107">Syntax</span></span>

<span data-ttu-id="c61e4-108">HASCATEGORY(\*\* *category* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c61e4-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c61e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c61e4-109">Parameters</span></span>

|<span data-ttu-id="c61e4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c61e4-110">**Name**</span></span>|<span data-ttu-id="c61e4-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c61e4-111">**Required/Optional**</span></span>|<span data-ttu-id="c61e4-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c61e4-112">**Data Type**</span></span>|<span data-ttu-id="c61e4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c61e4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c61e4-114">_category_</span><span class="sxs-lookup"><span data-stu-id="c61e4-114">_category_</span></span> <br/> |<span data-ttu-id="c61e4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c61e4-115">Required</span></span>  <br/> |<span data-ttu-id="c61e4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="c61e4-116">**String**</span></span> <br/> |<span data-ttu-id="c61e4-117">Die zu suchende Kategorie.</span><span class="sxs-lookup"><span data-stu-id="c61e4-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c61e4-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c61e4-118">Return value</span></span>

 <span data-ttu-id="c61e4-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c61e4-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c61e4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c61e4-120">Remarks</span></span>

 <span data-ttu-id="c61e4-121">*Kategorien*  sind benutzerdefinierte Zeichenfolgen, die Sie zum Kategorisieren von Shapes verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c61e4-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="c61e4-122">Kategorien können in der Zelle User.msvShapeCategories im ShapeSheet eines Shapes definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c61e4-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="c61e4-123">Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch Semikolons trennen.</span><span class="sxs-lookup"><span data-stu-id="c61e4-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

