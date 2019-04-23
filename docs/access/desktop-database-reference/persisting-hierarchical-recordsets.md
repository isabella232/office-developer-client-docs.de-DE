---
title: Speichern von hierarchische Recordsets
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287580"
---
# <a name="persisting-hierarchical-recordsets"></a>Speichern von hierarchische Recordsets

**Gilt für**: Access 2013, Office 2013

Sie können ein hierarchisches **Recordset** durch Aufrufen der [Save](save-method-ado.md)-Methode im ADTG- oder im XML-Format speichern. Beim Speichern hierarchischer **Recordset**-Objekte im XML-Format gelten jedoch zwei Einschränkungen: Das Speichern im XML-Format ist nicht möglich, wenn das hierarchische **Recordset**-Objekt ausstehende Aktualisierungen enthält, und es kann kein parametrisiertes hierarchisches **Recordset**-Objekt gespeichert werden.

For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).

