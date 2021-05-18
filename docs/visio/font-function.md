---
title: FONT Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine Schriftart zurück, der durch den Namen angegeben wird.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422173"
---
# <a name="font-function"></a><span data-ttu-id="76460-103">FONT Function</span><span class="sxs-lookup"><span data-stu-id="76460-103">FONT Function</span></span>

<span data-ttu-id="76460-104">Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine Schriftart zurück, der durch den Namen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76460-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="76460-105">In den meisten Fällen ist der Schriftartenbezeichner systemspezifisch.</span><span class="sxs-lookup"><span data-stu-id="76460-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="76460-106">Obwohl die Schriftart nach der Verwendung in einer Datei eingerichtet bleibt, bietet die **FONT-Funktion** einen konsistenten Zugriff auf eine bestimmte Schriftart über Systeme und Versionen von Visio.</span><span class="sxs-lookup"><span data-stu-id="76460-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="76460-107">Es wird empfohlen, die **FONT-Funktion** zu verwenden, um Schriftarten zuzuordnen, anstatt direkt auf Schriftartbezeichner zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="76460-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="76460-108">Informationen zur Version</span><span class="sxs-lookup"><span data-stu-id="76460-108">Version Information</span></span>

<span data-ttu-id="76460-109">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="76460-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76460-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="76460-110">Syntax</span></span>

 <span data-ttu-id="76460-111">**FONT**( _"font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="76460-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="76460-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="76460-112">Parameters</span></span>

|<span data-ttu-id="76460-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="76460-113">**Name**</span></span>|<span data-ttu-id="76460-114">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="76460-114">**Required/Optional**</span></span>|<span data-ttu-id="76460-115">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="76460-115">**Data Type**</span></span>|<span data-ttu-id="76460-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76460-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76460-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="76460-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="76460-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="76460-118">Required</span></span>  <br/> |<span data-ttu-id="76460-119">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="76460-119">**string**</span></span> <br/> |<span data-ttu-id="76460-120">Der Name der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="76460-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="76460-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76460-121">Return value</span></span>

<span data-ttu-id="76460-122">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="76460-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76460-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76460-123">Remarks</span></span>

<span data-ttu-id="76460-124">Wenn die für die  *Font_name_string*  bereitgestellte Zeichenfolge nicht mit einer bekannten Schriftart übereinstimmen, gibt diese Funktion eine #VALUE!</span><span class="sxs-lookup"><span data-stu-id="76460-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="76460-125">zurück.</span><span class="sxs-lookup"><span data-stu-id="76460-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="76460-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="76460-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="76460-127">Gibt den ganzzahligen Wert (4) zurück, der die eindeutige ID für die Schriftart "Calibri" darstellt.</span><span class="sxs-lookup"><span data-stu-id="76460-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

