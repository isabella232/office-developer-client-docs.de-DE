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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360165"
---
# <a name="hascategory-function"></a><span data-ttu-id="898c9-103">HASCATEGORY Function</span><span class="sxs-lookup"><span data-stu-id="898c9-103">HASCATEGORY Function</span></span>

<span data-ttu-id="898c9-104">Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.</span><span class="sxs-lookup"><span data-stu-id="898c9-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="898c9-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="898c9-105">Version Information</span></span>

<span data-ttu-id="898c9-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="898c9-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="898c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="898c9-107">Syntax</span></span>

<span data-ttu-id="898c9-108">HASCATEGORY (\* \* *Category* \* \*)</span><span class="sxs-lookup"><span data-stu-id="898c9-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="898c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="898c9-109">Parameters</span></span>

|<span data-ttu-id="898c9-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="898c9-110">**Name**</span></span>|<span data-ttu-id="898c9-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="898c9-111">**Required/Optional**</span></span>|<span data-ttu-id="898c9-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="898c9-112">**Data Type**</span></span>|<span data-ttu-id="898c9-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="898c9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="898c9-114">_Kategorie_</span><span class="sxs-lookup"><span data-stu-id="898c9-114">_category_</span></span> <br/> |<span data-ttu-id="898c9-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="898c9-115">Required</span></span>  <br/> |<span data-ttu-id="898c9-116">**String**</span><span class="sxs-lookup"><span data-stu-id="898c9-116">**String**</span></span> <br/> |<span data-ttu-id="898c9-117">Die zu suchende Kategorie.</span><span class="sxs-lookup"><span data-stu-id="898c9-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="898c9-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="898c9-118">Return value</span></span>

 <span data-ttu-id="898c9-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="898c9-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="898c9-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="898c9-120">Remarks</span></span>

 <span data-ttu-id="898c9-121">*Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, um Shapes zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="898c9-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="898c9-122">Kategorien können in der Zelle User.msvShapeCategories im ShapeSheet eines Shapes definiert werden.</span><span class="sxs-lookup"><span data-stu-id="898c9-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="898c9-123">Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch Semikolons trennen.</span><span class="sxs-lookup"><span data-stu-id="898c9-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

