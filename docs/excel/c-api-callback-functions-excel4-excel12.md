---
title: C-API-Rückruffunktionen Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen [Excel 2007], c-API-Rückruf
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434431"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="d68dd-104">C-API-Rückruffunktionen Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="d68dd-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="d68dd-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d68dd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d68dd-106">Die **Excel4** -und **Excel12** -Funktionen werden bereitgestellt, damit DLLs eine interne Microsoft Excel-Arbeitsblattfunktion, eine Makroblatt Funktion oder einen Befehl oder eine XLL-spezifische Funktion oder einen Befehl aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="d68dd-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="d68dd-107">Alle neueren Versionen von Excel unterstützen die **Excel4** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d68dd-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="d68dd-108">Ab Excel 2007 wird die **Excel12** -Funktion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d68dd-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="d68dd-109">Beide Funktionen werden in zwei Formen bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="d68dd-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="d68dd-110">Argumentlisten Formular mit variabler Länge (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="d68dd-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="d68dd-111">Ein Array-of-Arguments-Formular (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="d68dd-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="d68dd-112">Mit Ausnahme der Art und Weise, in der Argumente an diese Rückrufe übergeben werden, sind die beiden Formulare funktionell äquivalent.</span><span class="sxs-lookup"><span data-stu-id="d68dd-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="d68dd-113">Die grundlegenden Konzepte für beide Formulare werden vollständig in [Excel4/Excel12](excel4-excel12.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d68dd-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="d68dd-114">[Excel4v/Excel12v](excel4v-excel12v.md) behandelt andere Probleme zu diesem Formular.</span><span class="sxs-lookup"><span data-stu-id="d68dd-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d68dd-115">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="d68dd-115">In this section</span></span>

[<span data-ttu-id="d68dd-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="d68dd-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="d68dd-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="d68dd-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

