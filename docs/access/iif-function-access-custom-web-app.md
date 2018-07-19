---
title: IIf-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Überprüft, ob eine Bedingung erfüllt ist, und wenn true, wenn eine andere einen Wert zurück, auf If "FALSE".
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790179"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="e5f3c-103">IIf-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="e5f3c-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="e5f3c-104">Überprüft, ob eine Bedingung erfüllt ist, und wenn true, wenn eine andere einen Wert zurück, auf If "FALSE".</span><span class="sxs-lookup"><span data-stu-id="e5f3c-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e5f3c-p101"> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e5f3c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5f3c-107">Syntax</span></span>

<span data-ttu-id="e5f3c-108">**IIf** (*Bedingung*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="e5f3c-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="e5f3c-109">Die **IIf** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e5f3c-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="e5f3c-110">**Argument name**</span></span>|<span data-ttu-id="e5f3c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5f3c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e5f3c-112">*Bedingung*</span><span class="sxs-lookup"><span data-stu-id="e5f3c-112">*Condition*</span></span>  <br/> |<span data-ttu-id="e5f3c-113">Der Ausdruck, den ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="e5f3c-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="e5f3c-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="e5f3c-115">Wert oder-Ausdruck zurückgegeben, wenn *Bedingung* True ist.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="e5f3c-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="e5f3c-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="e5f3c-117">Wert oder-Ausdruck zurückgegeben, wenn *Bedingung* auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="e5f3c-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e5f3c-118">Example</span></span>

<span data-ttu-id="e5f3c-119">Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="e5f3c-120">Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5f3c-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


