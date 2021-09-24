---
title: Vermeiden von nicht unterstützten Technologien in verwalteten Outlook-Add-Ins
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e4572a7ed6ba2262874d03252f1bfb4adfefc82f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549749"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a>Vermeiden von nicht unterstützten Technologien in verwalteten Outlook-Add-Ins

Bestimmte Technologien, die für das .NET Framework galten, werden in der Programmierung von verwaltetem Code nicht unterstützt. Dazu gehören Datenobjekte für die Zusammenarbeit (Collaboration Data Objects, CDO), MAPI (Messaging Application Programming Interface, auch bekannt als Extended MAPI) und Simple MAPI. Diese Technologien wurden mit nicht verwaltetetem Code entworfen und entwickelt, und Microsoft stellt keine offiziell verwalteten Wrapper dafür zur Verfügung. 

Weitere Informationen finden Sie im Abschnitt „APIs that are supported in managed code“ im Artikel [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).

Microsoft Outlook bietet dennoch viele Objektmodellfeatures, mit denen erzielt werde kann, was bisher nur mit CDO und Exchange-Clienterweiterungen (ECE) für Entwickler gelöst werden konnte. Wenn Sie CDO in einer vorhandenen nicht verwalteten Outlook-Anwendung verwenden und die fehlende Unterstützung von CDO in verwalteten Lösungen Sie am Migrieren der Anwendung in verwalteten Code gehindert hat, können Sie nun überlegen, ob Sie Ihre Lösung mithilfe des Outlook-Objektmodells und der primären Interop-Assembly (PIA) auf verwalteteten Code aktualisieren, ohne dabei auf CDO zurückgreifen zu müssen. 

Weitere Informationen zur umfassenderen Outlook-Plattform und der reduzierten bedeutung von CDO und ECE in Outlook 2007 finden Sie unter [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).

