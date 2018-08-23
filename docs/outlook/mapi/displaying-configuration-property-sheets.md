---
title: Anzeigen der Konfiguration Eigenschaftenseiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588356"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="9833e-103">Anzeigen der Konfiguration Eigenschaftenseiten</span><span class="sxs-lookup"><span data-stu-id="9833e-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="9833e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9833e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9833e-105">Transportanbieter für verwenden Sie die Methode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) Konfiguration Eigenschaftenseiten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9833e-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="9833e-106">Beim Aufruf von **DoConfigPropSheet**übergibt der Adressbuchhierarchie einen Zeiger auf ein Array von Eigenschaften sowie Informationen dazu, wie sie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9833e-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="9833e-107">MAPI stellt dann die Eigenschaften für den Benutzer über ein standard-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="9833e-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="9833e-108">Es wird dringend empfohlen, diese Eigenschaft Blatt-Mechanismus verwenden, wenn Ihre Adressbuchhierarchie aufgrund der Vorteil für den Benutzer über eine konsistente Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="9833e-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="9833e-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="9833e-109">Transport providers</span></span>

<span data-ttu-id="9833e-110">Transportanbieter können die [BuildDisplayTable](builddisplaytable.md) -Funktion verwenden, um das Erstellen einer Tabelle anzeigen, für die Verwendung mit **DoConfigPropSheet**vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9833e-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="9833e-111">Transportanbieter können auch direkt auf die Eigenschaftenblatt-API zu.</span><span class="sxs-lookup"><span data-stu-id="9833e-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="9833e-112">Änderungen an den Eigenschaften Puffer, transport-Anbieter können die [CreateIProp](createiprop.md) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="9833e-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="9833e-113">Dies vereinfacht die Behandlung von Absagen vom Benutzer während der Benutzer die Werte in den Eigenschaften gespeichert geändert.</span><span class="sxs-lookup"><span data-stu-id="9833e-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="9833e-114">Wenn erforderlich, ein Transportdienstes auch ein Dialogfeld Assistent für bereitstellen kann im Feld, um die Konfigurationsaufgaben für den Benutzer zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9833e-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

