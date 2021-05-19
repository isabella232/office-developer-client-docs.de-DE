---
title: Try_Convert-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Konvertiert einen Wert in einen angegebenen Datentyp oder gibt Null zurück, wenn die Konvertierung ungültig ist.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410896"
---
# <a name="try_convert-function-access-custom-web-app"></a><span data-ttu-id="ab20e-103">Try_Convert-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="ab20e-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="ab20e-104">Konvertiert einen Wert in einen angegebenen Datentyp oder gibt Null zurück, wenn die Konvertierung ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="ab20e-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ab20e-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="ab20e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ab20e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab20e-107">Syntax</span></span>

 <span data-ttu-id="ab20e-108">**Try_Convert** (*DataType*, *Expression*)</span><span class="sxs-lookup"><span data-stu-id="ab20e-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="ab20e-109">Die **Try_Convert** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="ab20e-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ab20e-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="ab20e-110">**Argument name**</span></span>|<span data-ttu-id="ab20e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab20e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ab20e-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="ab20e-112">*DataType*</span></span>  <br/> |<span data-ttu-id="ab20e-113">Der Datentyp, in den Expression konvertiert *werden soll.*</span><span class="sxs-lookup"><span data-stu-id="ab20e-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="ab20e-114">*Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="ab20e-114">*Expression*</span></span>  <br/> |<span data-ttu-id="ab20e-115">Der wert, der konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab20e-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab20e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab20e-116">Remarks</span></span>

 <span data-ttu-id="ab20e-117">**Try_Convert** verwendet den übergebenen Wert und versucht, ihn in den angegebenen *DataType -Wert zu konvertieren.*</span><span class="sxs-lookup"><span data-stu-id="ab20e-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="ab20e-118">Wenn die Konvertierung erfolgreich ist, **gibt Try_Convert** den Wert als angegebenen  *DataType zurück.*  Wenn ein Fehler auftritt, wird null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab20e-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="ab20e-119">Wenn Sie jedoch eine Konvertierung anfordern, die explizit nicht zulässig ist, schlägt **Try_Convert** Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ab20e-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

