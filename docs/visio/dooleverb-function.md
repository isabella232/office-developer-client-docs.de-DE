---
title: DOOLEVERB-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Führt ein Verb für das OLE-Objekt aus.
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435662"
---
# <a name="dooleverb-function"></a><span data-ttu-id="46fa4-103">DOOLEVERB Function</span><span class="sxs-lookup"><span data-stu-id="46fa4-103">DOOLEVERB Function</span></span>

<span data-ttu-id="46fa4-104">Führt ein Verb für das OLE-Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="46fa4-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="46fa4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46fa4-105">Syntax</span></span>

<span data-ttu-id="46fa4-106">DOOLEVERB(" \*\* *verb* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="46fa4-106">DOOLEVERB(" \*\* *verb* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="46fa4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="46fa4-107">Parameters</span></span>

|<span data-ttu-id="46fa4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="46fa4-108">**Name**</span></span>|<span data-ttu-id="46fa4-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="46fa4-109">**Required/Optional**</span></span>|<span data-ttu-id="46fa4-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="46fa4-110">**Data Type**</span></span>|<span data-ttu-id="46fa4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46fa4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="46fa4-112">_"verb"_</span><span class="sxs-lookup"><span data-stu-id="46fa4-112">_"verb"_</span></span> <br/> |<span data-ttu-id="46fa4-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="46fa4-113">Required</span></span>  <br/> |<span data-ttu-id="46fa4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="46fa4-114">**String**</span></span> <br/> |<span data-ttu-id="46fa4-115">Die auszuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="46fa4-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46fa4-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46fa4-116">Remarks</span></span>

<span data-ttu-id="46fa4-p101">In früheren Versionen von Visio wird diese Funktion in der Form _DOOLEVERB angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an.</span><span class="sxs-lookup"><span data-stu-id="46fa4-p101">In earlier versions of Visio, this function appears as _DOOLEVERB. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="46fa4-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="46fa4-119">Example</span></span>

<span data-ttu-id="46fa4-120">DOOLEVERB("edit")</span><span class="sxs-lookup"><span data-stu-id="46fa4-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="46fa4-121">Ruft das Programm auf, aus dem das OLE-Objekt stammt, und öffnet das verknüpfte oder eingebettete Objekt zum Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="46fa4-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

