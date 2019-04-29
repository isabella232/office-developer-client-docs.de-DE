---
title: Anzeigen von Konfigurationseigenschaftenblättern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421312"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="5b175-103">Anzeigen von Konfigurationseigenschaftenblättern</span><span class="sxs-lookup"><span data-stu-id="5b175-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="5b175-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b175-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b175-105">Transport Anbieter verwenden die [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode, um Konfigurationseigenschaften Blätter zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5b175-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="5b175-106">Beim Aufrufen von **DoConfigPropSheet**übergibt der Transportanbieter einen Zeiger auf ein Array von Eigenschaften sowie Informationen dazu, wie diese angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5b175-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="5b175-107">Anschließend werden die Eigenschaften dem Benutzer mithilfe eines Standarddialogfelds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b175-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="5b175-108">Es wird dringend empfohlen, diesen Eigenschaftenblatt Mechanismus bei der Implementierung Ihres Transportanbieters zu verwenden, da der Benutzer eine konsistente Schnittstelle nutzen können.</span><span class="sxs-lookup"><span data-stu-id="5b175-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="5b175-109">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="5b175-109">Transport providers</span></span>

<span data-ttu-id="5b175-110">Transport Anbieter können die [BuildDisplayTable](builddisplaytable.md) -Funktion verwenden, um die Erstellung einer Anzeigetabelle für die Verwendung mit **DoConfigPropSheet**zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5b175-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="5b175-111">Transport Anbieter können auch die Eigenschaftenblatt-API direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b175-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="5b175-112">Zum Puffern von Änderungen an den Eigenschaften können Transportanbieter die [CreateIProp](createiprop.md) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b175-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="5b175-113">Dies vereinfacht die Behandlung von absagen durch den Benutzer, während der Benutzer die in den Eigenschaften gespeicherten Werte ändert.</span><span class="sxs-lookup"><span data-stu-id="5b175-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="5b175-114">Falls erforderlich, kann ein Transportanbieter auch ein Dialogfeld des Assistenten bereitstellen, um Konfigurationsaufgaben für den Benutzer zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5b175-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

