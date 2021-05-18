---
title: Verkettungsfunktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423272"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="ffb01-103">Verkettungsfunktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="ffb01-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="ffb01-104">Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.</span><span class="sxs-lookup"><span data-stu-id="ffb01-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ffb01-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="ffb01-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ffb01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb01-107">Syntax</span></span>

<span data-ttu-id="ffb01-108">**Concat** (*Value1*, *Value2*, ... [*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="ffb01-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="ffb01-109">Die Funktion **Verketten** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="ffb01-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ffb01-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="ffb01-110">**Argument Name**</span></span>|<span data-ttu-id="ffb01-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffb01-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffb01-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ffb01-112">Value</span></span>  <br/> |<span data-ttu-id="ffb01-113">Ein Zeichenfolgenwert, der mit den anderen Werten verkettet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffb01-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffb01-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffb01-114">Remarks</span></span>

<span data-ttu-id="ffb01-p102">**Verketten** verwendet eine unterschiedliche Anzahl von Zeichenfolgenargumenten und verkettet diese zu einer einzigen Zeichenfolge. Mindestens zwei Zeichenfolgenargumente sind erforderlich. Andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ffb01-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="ffb01-117">Alle Argumente werden implizit in Zeichenfolgen-Datentypen konvertiert und dann verkettet.</span><span class="sxs-lookup"><span data-stu-id="ffb01-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="ffb01-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ffb01-118">Example</span></span>

<span data-ttu-id="ffb01-119">Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält.</span><span class="sxs-lookup"><span data-stu-id="ffb01-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="ffb01-120">Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="ffb01-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


