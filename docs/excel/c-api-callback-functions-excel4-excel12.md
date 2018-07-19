---
title: C-API-Callback-Funktionen Excel4 Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen [excel 2007], C-API-Rückruf
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 221ea4c9c706d11acd31d3f2870d326a7189d299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790380"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="5252b-104">C-API-Callback-Funktionen Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="5252b-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="5252b-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5252b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5252b-106">Die **Excel4** und **Excel12** -Funktionen werden bereitgestellt, um DLLs aufrufen, einen internen Microsoft Excel-Arbeitsblatt-Funktion, Blatt Makrofunktion oder Befehl oder XLL-only Sonderfunktion oder Befehl aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5252b-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="5252b-107">Alle aktuelle Versionen von Excel unterstützen die **Excel4** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5252b-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="5252b-108">Ab Excel 2007 **mit Excel12** -Funktion wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5252b-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="5252b-109">Beide Funktionen werden in zwei Formen bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="5252b-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="5252b-110">Listenformular variabler Länge Argument (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="5252b-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="5252b-111">Ein Array von Argumenten-Formular (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="5252b-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="5252b-112">Mit Ausnahme wie in der Argumente an diese Rückrufe übergeben werden, sind die beiden Formen funktional.</span><span class="sxs-lookup"><span data-stu-id="5252b-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="5252b-113">Die grundlegenden Konzepte für beide Formulare werden vollständig in [Excel4/Excel12](excel4-excel12.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5252b-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="5252b-114">[Excel4v/Excel12v](excel4v-excel12v.md) werden andere Probleme zu diesem Formular behandelt.</span><span class="sxs-lookup"><span data-stu-id="5252b-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="5252b-115">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="5252b-115">In this section</span></span>

[<span data-ttu-id="5252b-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="5252b-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="5252b-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="5252b-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

