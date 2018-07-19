---
title: FONT Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Gibt den Integer-Wert, der den eindeutigen Bezeichner für eine Schriftart, die durch Name angegebene zurück.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797050"
---
# <a name="font-function"></a><span data-ttu-id="a9bb0-103">FONT Function</span><span class="sxs-lookup"><span data-stu-id="a9bb0-103">FONT Function</span></span>

<span data-ttu-id="a9bb0-104">Gibt den Integer-Wert, der den eindeutigen Bezeichner für eine Schriftart, die durch Name angegebene zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a9bb0-105">In den meisten Fällen wird die Schriftart-ID systemspezifische.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="a9bb0-106">Obwohl die Schriftart eingerichteten einmal in einer Datei verwendet bleibt, stellt die **Schriftart** Funktion konsistenten Zugriff auf eine bestimmte Schriftart System-und Versionen von Visio an.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="a9bb0-107">Es wird empfohlen, für die Verwendung der Funktion **Schriftart** Schriftarten anstatt direkt in Bezug auf die Schriftart Bezeichner zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="a9bb0-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="a9bb0-108">Version Information</span></span>

<span data-ttu-id="a9bb0-109">Hinzugefügte Version: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="a9bb0-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a9bb0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9bb0-110">Syntax</span></span>

 <span data-ttu-id="a9bb0-111">**Schriftart** ( _"Font_name_string"_)</span><span class="sxs-lookup"><span data-stu-id="a9bb0-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="a9bb0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bb0-112">Parameters</span></span>

|<span data-ttu-id="a9bb0-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9bb0-113">**Name**</span></span>|<span data-ttu-id="a9bb0-114">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a9bb0-114">**Required/Optional**</span></span>|<span data-ttu-id="a9bb0-115">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a9bb0-115">**Data Type**</span></span>|<span data-ttu-id="a9bb0-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9bb0-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9bb0-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="a9bb0-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="a9bb0-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9bb0-118">Required</span></span>  <br/> |<span data-ttu-id="a9bb0-119">**string**</span><span class="sxs-lookup"><span data-stu-id="a9bb0-119">**string**</span></span> <br/> |<span data-ttu-id="a9bb0-120">Der Name der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="a9bb0-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9bb0-121">Return value</span></span>

<span data-ttu-id="a9bb0-122">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="a9bb0-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9bb0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9bb0-123">Remarks</span></span>

<span data-ttu-id="a9bb0-124">Wenn die Zeichenfolge *Font_name_string* vorgesehenen nicht über eine bekannte Schriftart übereinstimmt, gibt diese Funktion ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a9bb0-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="a9bb0-125">Fehler.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a9bb0-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9bb0-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="a9bb0-127">Gibt den ganzzahligen Wert (4), die eindeutige ID für die Schriftart "Calibri" darstellt.</span><span class="sxs-lookup"><span data-stu-id="a9bb0-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

