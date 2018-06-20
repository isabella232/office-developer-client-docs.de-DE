---
title: Zelle "Ask" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796393"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="3bd69-103">Zelle "Ask" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="3bd69-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="3bd69-104">Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.</span><span class="sxs-lookup"><span data-stu-id="3bd69-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="3bd69-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3bd69-105">**Value**</span></span>|<span data-ttu-id="3bd69-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bd69-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3bd69-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3bd69-107">TRUE</span></span>  <br/> |<span data-ttu-id="3bd69-108">Auffordern Sie Benutzer zu Shape-Daten in das Dialogfeld **Shape-Daten definieren** einzugeben.</span><span class="sxs-lookup"><span data-stu-id="3bd69-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="3bd69-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3bd69-109">FALSE</span></span>  <br/> |<span data-ttu-id="3bd69-110">Bitten Sie die Benutzer Daten eingeben nicht.</span><span class="sxs-lookup"><span data-stu-id="3bd69-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bd69-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3bd69-111">Remarks</span></span>

<span data-ttu-id="3bd69-112">Der Wert in dieser Zelle entspricht dem Kontrollkästchen **beim Ablegen fragen** im Dialogfeld **Shape-Daten definieren** (mit der rechten Maustaste in des Shapes, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).</span><span class="sxs-lookup"><span data-stu-id="3bd69-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="3bd69-113">Zum Abrufen eines Verweises auf die Zelle Ask nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3bd69-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bd69-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3bd69-114">Cell name:</span></span>  <br/> |<span data-ttu-id="3bd69-115">Eigenschaft. *Name* . Stellen Sie sicher, auf dem Prop.  *Name* ist der Name der Zeile mit der benutzerdefinierten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3bd69-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="3bd69-116">Wenn Sie einen Verweis auf die Zelle Ask aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3bd69-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bd69-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3bd69-117">Section index:</span></span>  <br/> |<span data-ttu-id="3bd69-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="3bd69-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="3bd69-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3bd69-119">Row index:</span></span>  <br/> |<span data-ttu-id="3bd69-120">**VisRowProp** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="3bd69-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="3bd69-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3bd69-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3bd69-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="3bd69-122">**visCustPropsAsk**</span></span> <br/> |
   

