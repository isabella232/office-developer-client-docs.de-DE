---
title: SetReturnVar-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Die SetReturnVar-Aktion erstellt eine Variable zurückgegebene und platziert es in einem bestimmten Wert.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790381"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="0466e-103">SetReturnVar-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="0466e-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="0466e-104">Die **SetReturnVar** -Aktion erstellt eine Variable zurückgegebene und platziert es in einem bestimmten Wert.</span><span class="sxs-lookup"><span data-stu-id="0466e-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0466e-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="0466e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0466e-107">Die **SetReturnVar** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0466e-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="0466e-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="0466e-108">Setting</span></span>

<span data-ttu-id="0466e-109">Die **SetReturnVar** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="0466e-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="0466e-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="0466e-110">**Argument name**</span></span>|<span data-ttu-id="0466e-111">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0466e-111">**Required**</span></span>|<span data-ttu-id="0466e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0466e-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0466e-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="0466e-113">_Name_</span></span> <br/> |<span data-ttu-id="0466e-114">Ja</span><span class="sxs-lookup"><span data-stu-id="0466e-114">Yes</span></span>  <br/> |<span data-ttu-id="0466e-115">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="0466e-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="0466e-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="0466e-116">_Expression_</span></span> <br/> |<span data-ttu-id="0466e-117">Ja</span><span class="sxs-lookup"><span data-stu-id="0466e-117">Yes</span></span>  <br/> |<span data-ttu-id="0466e-118">Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0466e-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="0466e-119">Setzen Sie den Ausdruck mit dem Gleichheitszeichen (=).</span><span class="sxs-lookup"><span data-stu-id="0466e-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="0466e-120">Sie können klicken Sie auf die Schaltfläche **Erstellen** , um den **Ausdrucks-Generator** verwenden, um dieses Argument festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0466e-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0466e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0466e-121">Remarks</span></span>

<span data-ttu-id="0466e-122">Die Aktion **SetReturnVar** dient zum Erstellen einer **ReturnVar**die Variable, die von Makros kann, die ein Datenmakro Aufrufen verwendet werden, indem Sie mit der **AusführenDatenmakro** -Aktion ist.</span><span class="sxs-lookup"><span data-stu-id="0466e-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="0466e-123">Nach dem Erstellen einer **ReturnVar** durch die **SetReturnVar** -Aktion können Sie von das aufrufende Makro in einem Ausdruck verwenden.</span><span class="sxs-lookup"><span data-stu-id="0466e-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="0466e-124">Angenommen, wenn Sie eine **ReturnVar** mit dem Namen **UpdateSuccess**erstellt, können die Variable Sie mithilfe der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="0466e-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="0466e-125">Die **SetReturnVar** -Aktion kann nur in benannten Datenmakros verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0466e-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="0466e-126">Es ist nicht verfügbar in Datenmakros, die ein Ereignis eines Makro zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0466e-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

