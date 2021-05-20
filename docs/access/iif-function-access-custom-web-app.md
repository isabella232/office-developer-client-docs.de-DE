---
title: IIf-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn TRUE eines anderen auf ist, wenn sie FALSE ist.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439079"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="0f637-103">IIf-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="0f637-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="0f637-104">Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn TRUE eines anderen auf ist, wenn sie FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="0f637-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0f637-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="0f637-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0f637-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f637-107">Syntax</span></span>

<span data-ttu-id="0f637-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="0f637-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="0f637-109">Die **IIf-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="0f637-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="0f637-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="0f637-110">**Argument name**</span></span>|<span data-ttu-id="0f637-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f637-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0f637-112">*Bedingung*</span><span class="sxs-lookup"><span data-stu-id="0f637-112">*Condition*</span></span>  <br/> |<span data-ttu-id="0f637-113">Der Ausdruck, den Sie auswerten möchten.</span><span class="sxs-lookup"><span data-stu-id="0f637-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="0f637-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="0f637-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="0f637-115">Wert oder Ausdruck zurückgegeben, wenn  *Condition*  true ist.</span><span class="sxs-lookup"><span data-stu-id="0f637-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="0f637-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="0f637-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="0f637-117">Zurückgegebener Wert oder Ausdruck, wenn  *Condition auf*  False gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="0f637-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="0f637-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0f637-118">Example</span></span>

<span data-ttu-id="0f637-119">Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält.</span><span class="sxs-lookup"><span data-stu-id="0f637-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="0f637-120">Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="0f637-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


