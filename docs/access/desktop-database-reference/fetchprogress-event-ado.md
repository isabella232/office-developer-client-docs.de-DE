---
title: FetchProgress-Ereignis (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72a860ecd52e0481b55423f88e537eab3c8de2ae
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474386"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress-Ereignis (ADO)


**Betrifft**: Access 2013 | Office 2013


Das **FetchProgress** -Ereignis wird regelmäßig während einer langen asynchronen Operation aufgerufen, um einen Bericht darüber zu erstellen, wie viele zusätzliche Zeilen derzeit in das [Recordset](recordset-object-ado.md) abgerufen wurden.

## <a name="syntax"></a>Syntax

FetchProgress*Fortschritt*, *MaxProgress*, *AdStatus*, *pCommand*

## <a name="parameters"></a>Parameter

  - *Progress*

  - Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, die derzeit mit der Fetch-Operation abgerufen wurden.

  - *MaxProgress*

  - Ein **Long** -Wert, der die maximale Anzahl von Datensätzen angibt, die erwartungsgemäß abgerufen werden.

  - *adStatus*

  - Ein [EventStatusEnum](eventstatusenum.md)-Statuswert.

  - *pCommand*

  - Ein **Recordset** -Objekt, das das Objekt darstellt, für das die Datensätze abgerufen werden.

## <a name="remarks"></a>Hinweise

Wenn **FetchProgress** mit einem untergeordneten **Recordset-Objekt**verwendet, achten Sie darauf, dass die Parameterwerte *des Fortschritts* und der *MaxProgress* aus dem zugrunde liegenden [Cursordiensts](microsoft-cursor-service-for-ole-db-ado-service-component.md) Rowset abgeleitet sind. Die zurückgegebenen Werte stellen die Gesamtanzahl von Datensätzen im zugrunde liegenden Rowset dar, nicht nur die Anzahl von Datensätzen im aktuellen Kapitel.


> [!NOTE]
> <P>[!HINWEIS] Um <STRONG>FetchProgress</STRONG> mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.</P>


