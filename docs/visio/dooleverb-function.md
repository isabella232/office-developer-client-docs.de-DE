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
description: Führt eine Aktion für das OLE-Objekt.
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796884"
---
# <a name="dooleverb-function"></a><span data-ttu-id="3cb14-103">DOOLEVERB-Funktion</span><span class="sxs-lookup"><span data-stu-id="3cb14-103">DOOLEVERB Function</span></span>

<span data-ttu-id="3cb14-104">Führt eine Aktion für das OLE-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb14-104">Executes a verb for the OLE object.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3cb14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cb14-105">Syntax</span></span>

<span data-ttu-id="3cb14-106">DOOLEVERB ("** *Verb* **")</span><span class="sxs-lookup"><span data-stu-id="3cb14-106">DOOLEVERB(" ** *verb* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3cb14-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cb14-107">Parameters</span></span>

|<span data-ttu-id="3cb14-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3cb14-108">**Name**</span></span>|<span data-ttu-id="3cb14-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3cb14-109">**Required/Optional**</span></span>|<span data-ttu-id="3cb14-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3cb14-110">**Data Type**</span></span>|<span data-ttu-id="3cb14-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3cb14-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3cb14-112">_"Verb"_</span><span class="sxs-lookup"><span data-stu-id="3cb14-112">_"verb"_</span></span> <br/> |<span data-ttu-id="3cb14-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3cb14-113">Required</span></span>  <br/> |<span data-ttu-id="3cb14-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3cb14-114">**String**</span></span> <br/> |<span data-ttu-id="3cb14-115">Die auszuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="3cb14-115">The verb to execute.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cb14-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cb14-116">Remarks</span></span>

<span data-ttu-id="3cb14-p101">In früheren Versionen von Visio wird diese Funktion in der Form _DOOLEVERB angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an.</span><span class="sxs-lookup"><span data-stu-id="3cb14-p101">In earlier versions of Visio, this function appears as _DOOLEVERB. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3cb14-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3cb14-119">Example</span></span>

<span data-ttu-id="3cb14-120">DOOLEVERB("edit")</span><span class="sxs-lookup"><span data-stu-id="3cb14-120">DOOLEVERB("edit")</span></span>
  
<span data-ttu-id="3cb14-121">Ruft das Programm auf, aus dem das OLE-Objekt stammt, und öffnet das verknüpfte oder eingebettete Objekt zum Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3cb14-121">Runs the OLE object program and displays the linked or embedded object so that it can be edited.</span></span>
  

