---
title: Concat-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790171"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="cc5ba-103">Concat-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="cc5ba-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="cc5ba-104">Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cc5ba-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cc5ba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc5ba-107">Syntax</span></span>

<span data-ttu-id="cc5ba-108">**Concat** (*Wert1*, *Wert2*... [*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="cc5ba-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="cc5ba-109">Die Funktion **Verketten** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="cc5ba-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="cc5ba-110">**Argument Name**</span></span>|<span data-ttu-id="cc5ba-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc5ba-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc5ba-112">Wert</span><span class="sxs-lookup"><span data-stu-id="cc5ba-112">Value</span></span>  <br/> |<span data-ttu-id="cc5ba-113">Ein Zeichenfolgenwert, der mit den anderen Werten verkettet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc5ba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc5ba-114">Remarks</span></span>

<span data-ttu-id="cc5ba-p102">**Verketten** verwendet eine unterschiedliche Anzahl von Zeichenfolgenargumenten und verkettet diese zu einer einzigen Zeichenfolge. Mindestens zwei Zeichenfolgenargumente sind erforderlich. Andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="cc5ba-117">Alle Argumente werden implizit in Zeichenfolgen-Datentypen konvertiert und dann verkettet.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="cc5ba-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cc5ba-118">Example</span></span>

<span data-ttu-id="cc5ba-119">Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="cc5ba-120">Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc5ba-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


