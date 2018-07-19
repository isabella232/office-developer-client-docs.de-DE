---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Der Vergleichsvorgänge zwischen anderen Sprache Darstellungen ermöglicht. Es ist am besten für die Konvertierung von Tags (BCP 47) Werte der Internet Engineering Task Force Language, Werte für den Gebietsschemabezeichner (LCID) verwendet.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797298"
---
# <a name="language-function"></a><span data-ttu-id="f69d1-104">LANGUAGE Function</span><span class="sxs-lookup"><span data-stu-id="f69d1-104">LANGUAGE Function</span></span>

<span data-ttu-id="f69d1-105">Der Vergleichsvorgänge zwischen anderen Sprache Darstellungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f69d1-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="f69d1-106">Es ist am besten für die Konvertierung von Tags (BCP 47) Werte der Internet Engineering Task Force Language, Werte für den Gebietsschemabezeichner (LCID) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f69d1-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="f69d1-107">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="f69d1-107">Version Information</span></span>

<span data-ttu-id="f69d1-108">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="f69d1-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f69d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f69d1-109">Syntax</span></span>

 <span data-ttu-id="f69d1-110">**Sprache** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="f69d1-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="f69d1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f69d1-111">Parameters</span></span>

|<span data-ttu-id="f69d1-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="f69d1-112">**Name**</span></span>|<span data-ttu-id="f69d1-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f69d1-113">**Required/Optional**</span></span>|<span data-ttu-id="f69d1-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f69d1-114">**Data Type**</span></span>|<span data-ttu-id="f69d1-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f69d1-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f69d1-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="f69d1-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="f69d1-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f69d1-117">Required</span></span>  <br/> |<span data-ttu-id="f69d1-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f69d1-118">**String**</span></span> <br/> |<span data-ttu-id="f69d1-119">Der LCID oder BCP 47 Wert für die Sprache.</span><span class="sxs-lookup"><span data-stu-id="f69d1-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="f69d1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f69d1-120">Return value</span></span>

<span data-ttu-id="f69d1-121">Integer</span><span class="sxs-lookup"><span data-stu-id="f69d1-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="f69d1-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f69d1-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="f69d1-123">Gibt den Wert "1033" zurück.</span><span class="sxs-lookup"><span data-stu-id="f69d1-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="f69d1-124">Gibt den Wert "3082" zurück.</span><span class="sxs-lookup"><span data-stu-id="f69d1-124">Returns a value of '3082'.</span></span>
  

