---
title: Installieren der Outlook-PIA und Verweisen auf diese
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718203"
---
# <a name="installing-and-referencing-the-outlook-pia"></a><span data-ttu-id="cf712-102">Installieren der Outlook-PIA und Verweisen auf diese</span><span class="sxs-lookup"><span data-stu-id="cf712-102">Installing and referencing the Outlook PIA</span></span>

<span data-ttu-id="cf712-103">Bevor Sie Informationen aus der primären Interopassembly (PIA) von Outlook in ein verwaltetes Outlook-Add-In integrieren können, müssen Sie die PIA im globalen Assemblycache (GAC) installieren.</span><span class="sxs-lookup"><span data-stu-id="cf712-103">You must have the Outlook Primary Interop Assembly (PIA) installed in the Global Assembly Cache (GAC) before you can incorporate information from the PIA in an Outlook managed add-in.</span></span> <span data-ttu-id="cf712-104">Standardmäßig wird die PIA automatisch bei der Installation von Office auf dem Entwicklungscomputer installiert.</span><span class="sxs-lookup"><span data-stu-id="cf712-104">By default, the PIA is installed automatically when you install Office on the development computer.</span></span> <span data-ttu-id="cf712-105">Wenn Sie die PIA jedoch separat installieren müssen, finden Sie weitere Informationen unter [Konfigurieren eines Computers zum Entwickeln von Office-Lösungen](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="cf712-105">However, if you need to install the PIA separately, see [Configure a computer to develop Office solutions](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span></span>


> [!NOTE] 
> <span data-ttu-id="cf712-106">Sie müssen ein Administrator auf dem Entwicklungscomputer sein, um die Office-PIAs zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cf712-106">You must be an administrator on the development computer to install the Office PIAs.</span></span>

<span data-ttu-id="cf712-p102">Wenn Sie nach der Installation das verwaltete Projekt in Visual Studio erstellen, können Sie einen Verweis auf die Komponente Microsoft Outlook 15.0-Objektbibliothek hinzufügen. Anschließend werden im Objektkatalog unter dem Namespace **Microsoft.Office.Interop.Outlook** verwaltete Schnittstellen in der PIA angezeigt, deren Namen Objekten im Outlook-Objektmodell entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cf712-p102">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the Microsoft Outlook 15.0 Object Library component. Subsequently, in the object browser, under the **Microsoft.Office.Interop.Outlook** namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf712-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf712-109">See also</span></span>

- [<span data-ttu-id="cf712-110">Installieren von primären Interop-Assemblys für Office</span><span class="sxs-lookup"><span data-stu-id="cf712-110">Install Office primary interop assemblies</span></span>](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [<span data-ttu-id="cf712-111">Architektur der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="cf712-111">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)

