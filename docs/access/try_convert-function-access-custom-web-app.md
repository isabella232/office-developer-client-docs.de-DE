---
title: Try_Convert-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Konvertiert einen Wert in einem angegebenen Datentyp, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790395"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="0a20a-103">Try_Convert-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="0a20a-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="0a20a-104">Konvertiert einen Wert in einem angegebenen Datentyp, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0a20a-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0a20a-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="0a20a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0a20a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a20a-107">Syntax</span></span>

 <span data-ttu-id="0a20a-108">**Try_Convert** (*Datentyp*, *Ausdruck*)</span><span class="sxs-lookup"><span data-stu-id="0a20a-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="0a20a-109">Die **Try_Convert** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="0a20a-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="0a20a-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="0a20a-110">**Argument name**</span></span>|<span data-ttu-id="0a20a-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a20a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0a20a-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="0a20a-112">*DataType*</span></span>  <br/> |<span data-ttu-id="0a20a-113">Geben Sie die Daten in den *Ausdruck* konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0a20a-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="0a20a-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="0a20a-114">*Expression*</span></span>  <br/> |<span data-ttu-id="0a20a-115">Der Wert konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a20a-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a20a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a20a-116">Remarks</span></span>

 <span data-ttu-id="0a20a-117">**Try_Convert** nimmt den Wert übergeben wurden und versucht, in den angegebenen *Datentyp* zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0a20a-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="0a20a-118">Wenn die Konvertierung erfolgreich ist, gibt **Try_Convert** den Wert als den angegebenen *Datentyp* zurück; Wenn ein Fehler auftritt, wird Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a20a-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="0a20a-119">Jedoch wenn Sie eine Konvertierung, die nicht explizit zulässig ist anfordern, schlägt **Try_Convert** mit einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="0a20a-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

