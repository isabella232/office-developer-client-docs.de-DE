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
description: Führt den identifizierten Befehl aus.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315232"
---
# <a name="docmd-function"></a><span data-ttu-id="db1ea-103">DOCMD Function</span><span class="sxs-lookup"><span data-stu-id="db1ea-103">DOCMD Function</span></span>

<span data-ttu-id="db1ea-104">Führt den identifizierten Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="db1ea-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="db1ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db1ea-105">Syntax</span></span>

 <span data-ttu-id="db1ea-106">**DoCmd** ( _CommandID_)</span><span class="sxs-lookup"><span data-stu-id="db1ea-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="db1ea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="db1ea-107">Parameters</span></span>

|<span data-ttu-id="db1ea-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="db1ea-108">**Name**</span></span>|<span data-ttu-id="db1ea-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="db1ea-109">**Required/Optional**</span></span>|<span data-ttu-id="db1ea-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="db1ea-110">**Data Type**</span></span>|<span data-ttu-id="db1ea-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db1ea-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="db1ea-112">_commandID_</span><span class="sxs-lookup"><span data-stu-id="db1ea-112">_commandID_</span></span> <br/> |<span data-ttu-id="db1ea-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="db1ea-113">Required</span></span>  <br/> |<span data-ttu-id="db1ea-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="db1ea-114">**Number**</span></span> <br/> | <span data-ttu-id="db1ea-115">Der auszuführende Befehl.</span><span class="sxs-lookup"><span data-stu-id="db1ea-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db1ea-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db1ea-116">Remarks</span></span>

<span data-ttu-id="db1ea-117">Eine Liste der Befehle, die mit der DOCMD-Funktion unterstützt werden, finden Sie im Thema "DoCmd/DOCMD-Befehle" in der Microsoft Visio 2013-AutomatisierungsReferenz.</span><span class="sxs-lookup"><span data-stu-id="db1ea-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="db1ea-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="db1ea-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="db1ea-119">Bewirkt, dass das Dialogfeld **Shape-Daten** auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="db1ea-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

