---
title: Microsoft Cursor Service für OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314357"
---
# <a name="microsoft-cursor-service-for-ole-db"></a>Microsoft Cursor Service für OLE DB


**Gilt für**: Access 2013, Office 2013

Wenn Sie einen clientseitigen Cursor auswählen oder die **CursorLocation** -Eigenschaft auf **adUseClient** festlegen, wird der Microsoft Cursor Service für OLE DB aufgerufen. Möglicherweise werden auch Verweise auf "Client Cursor Engine" angezeigt, wobei es sich im Prinzip um die Entsprechung im ADO-Kontext handelt. Dieser Dienst ergänzt die Cursorunterstützungsfunktionen von Datenprovidern. Sie erhalten daher relativ einheitliche Funktionalität von allen Datenprovidern.

Der Microsoft Cursor Service für OLE DB stellt dynamische Eigenschaften bereit und optimiert das Verhalten bestimmter Methoden. Beispielsweise können mit der dynamischen Eigenschaft **Optimize** temporäre Indizes erstellt werden, um bestimmte Vorgänge zu ermöglichen, wie z. B. die **Find** -Methode.

Der Microsoft Cursor Service für OLE DB ermöglicht die Unterstützung der Batchaktualisierung in allen Fällen. Er simuliert außerdem leistungsfähigere Cursortypen, wie z. B. dynamische Cursor, wenn ein Datenprovider nur weniger leistungsfähige Cursor bereitstellen kann, wie z. B. statische Cursor.

