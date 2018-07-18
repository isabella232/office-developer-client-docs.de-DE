---
title: DOCMD-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Führt den angegebenen Befehl.
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796868"
---
# <a name="docmd-function"></a><span data-ttu-id="972b3-103">DOCMD Function</span><span class="sxs-lookup"><span data-stu-id="972b3-103">DOCMD Function</span></span>

<span data-ttu-id="972b3-104">Führt den angegebenen Befehl.</span><span class="sxs-lookup"><span data-stu-id="972b3-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="972b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="972b3-105">Syntax</span></span>

 <span data-ttu-id="972b3-106">**DOCMD** ( _CommandID_)</span><span class="sxs-lookup"><span data-stu-id="972b3-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="972b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="972b3-107">Parameters</span></span>

|<span data-ttu-id="972b3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="972b3-108">**Name**</span></span>|<span data-ttu-id="972b3-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="972b3-109">**Required/Optional**</span></span>|<span data-ttu-id="972b3-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="972b3-110">**Data Type**</span></span>|<span data-ttu-id="972b3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="972b3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="972b3-112">_commandID_</span><span class="sxs-lookup"><span data-stu-id="972b3-112">_commandID_</span></span> <br/> |<span data-ttu-id="972b3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="972b3-113">Required</span></span>  <br/> |<span data-ttu-id="972b3-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="972b3-114">**Number**</span></span> <br/> | <span data-ttu-id="972b3-115">Der auszuführende Befehl.</span><span class="sxs-lookup"><span data-stu-id="972b3-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="972b3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="972b3-116">Remarks</span></span>

<span data-ttu-id="972b3-117">Eine Liste der Befehle, die mit der DOCMD-Funktion unterstützt werden, finden Sie unter dem Thema "DoCmd/DOCMD-Befehle" in der Microsoft Visio 2013-Automatisierungsreferenz.</span><span class="sxs-lookup"><span data-stu-id="972b3-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="972b3-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="972b3-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="972b3-119">Bewirkt, dass das Dialogfeld **Shape-Daten** auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="972b3-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

