---
title: LANGUAGE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Ermöglicht Vergleichsvorgänge zwischen verschiedenen sprach Darstellungen. Es wird am besten für die Konvertierung von Internet Engineering Task Force Language Tags (BCP 47)-Werten in Gebietsschema-ID (LCID)-Werte verwendet.
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424752"
---
# <a name="language-function"></a><span data-ttu-id="4b91b-104">LANGUAGE-Funktion</span><span class="sxs-lookup"><span data-stu-id="4b91b-104">LANGUAGE Function</span></span>

<span data-ttu-id="4b91b-105">Ermöglicht Vergleichsvorgänge zwischen verschiedenen sprach Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="4b91b-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="4b91b-106">Es wird am besten für die Konvertierung von Internet Engineering Task Force Language Tags (BCP 47)-Werten in Gebietsschema-ID (LCID)-Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b91b-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4b91b-107">Informationen zur Version</span><span class="sxs-lookup"><span data-stu-id="4b91b-107">Version Information</span></span>

<span data-ttu-id="4b91b-108">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="4b91b-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4b91b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b91b-109">Syntax</span></span>

 <span data-ttu-id="4b91b-110">**Sprache** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="4b91b-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="4b91b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b91b-111">Parameters</span></span>

|<span data-ttu-id="4b91b-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="4b91b-112">**Name**</span></span>|<span data-ttu-id="4b91b-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="4b91b-113">**Required/Optional**</span></span>|<span data-ttu-id="4b91b-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4b91b-114">**Data Type**</span></span>|<span data-ttu-id="4b91b-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4b91b-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4b91b-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="4b91b-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="4b91b-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4b91b-117">Required</span></span>  <br/> |<span data-ttu-id="4b91b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="4b91b-118">**String**</span></span> <br/> |<span data-ttu-id="4b91b-119">Der LCID-oder BCP 47-Wert für die Sprache.</span><span class="sxs-lookup"><span data-stu-id="4b91b-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="4b91b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b91b-120">Return value</span></span>

<span data-ttu-id="4b91b-121">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="4b91b-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="4b91b-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4b91b-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="4b91b-123">Gibt den Wert "1033" zurück.</span><span class="sxs-lookup"><span data-stu-id="4b91b-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="4b91b-124">Gibt den Wert "3082" zurück.</span><span class="sxs-lookup"><span data-stu-id="4b91b-124">Returns a value of '3082'.</span></span>
  

