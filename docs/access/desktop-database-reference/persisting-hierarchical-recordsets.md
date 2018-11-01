---
title: Speichern hierarchischer Recordsets
TOCTitle: Persisting Hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c990ef345ed8e10223757ded958b1b8a0f60eb26
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877380"
---
# <a name="persisting-hierarchical-recordsets"></a>Speichern hierarchischer Recordsets


**Betrifft**: Access 2013, Office 2013

Sie können ein hierarchisches **Recordset** durch Aufrufen der [Save](save-method-ado.md)-Methode im ADTG- oder im XML-Format speichern. Beim Speichern hierarchischer **Recordset**-Objekte im XML-Format gelten jedoch zwei Einschränkungen: Das Speichern im XML-Format ist nicht möglich, wenn das hierarchische **Recordset**-Objekt ausstehende Aktualisierungen enthält, und es kann kein parametrisiertes hierarchisches **Recordset**-Objekt gespeichert werden.

Weitere Informationen zum Datenstrukturierungsanbieter finden Sie unter Microsoft Data Shaping Dienst für OLE DB (ADO) und Der Data Shaping Dienst für OLE DB (OLE DB).

