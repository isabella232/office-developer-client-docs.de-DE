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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336876"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Installieren der Outlook-PIA und Verweisen auf diese

Bevor Sie Informationen aus der primären Interopassembly (PIA) von Outlook in ein verwaltetes Outlook-Add-In integrieren können, müssen Sie die PIA im globalen Assemblycache (GAC) installieren. Standardmäßig wird die PIA automatisch bei der Installation von Office auf dem Entwicklungscomputer installiert. Wenn Sie die PIA jedoch separat installieren müssen, finden Sie weitere Informationen unter [Konfigurieren eines Computers zum Entwickeln von Office-Lösungen](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).


> [!NOTE] 
> Sie müssen ein Administrator auf dem Entwicklungscomputer sein, um die Office-PIAs zu installieren.

Wenn Sie nach der Installation das verwaltete Projekt in Visual Studio erstellen, können Sie einen Verweis auf die Komponente Microsoft Outlook 15.0-Objektbibliothek hinzufügen. Anschließend werden im Objektkatalog unter dem Namespace **Microsoft.Office.Interop.Outlook** verwaltete Schnittstellen in der PIA angezeigt, deren Namen Objekten im Outlook-Objektmodell entsprechen.

## <a name="see-also"></a>Siehe auch

- [Installieren von primären Interop-Assemblys für Office](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Architektur der Outlook-PIA](architecture-of-the-outlook-pia.md)

