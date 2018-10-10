---
title: MarshalOptions-Eigenschaft (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475197"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.

## <a name="remarks"></a>Hinweise

Bei der Verwendung eines clientseitigen [Recordsets](recordset-object-ado.md) werden Datensätze, die auf dem Client geändert wurden, wieder auf die mittlere Stufe bzw. den Webserver zurückgeschrieben. Das hierbei verwendete Verfahren wird Marshalling genannt. Dabei handelt es sich um das thread- oder prozessübergreifende Packen und Senden von Methodenparametern der Schnittstelle. Das Festlegen der **MarshalOptions** -Eigenschaft kann die Leistung verbessern, wenn geänderte Remotedaten zur Aktualisierung zurück auf die mittlere Stufe bzw. den Webserver gemarshallt werden.

**Remote Data Service-Verwendung** Diese Eigenschaft wird nur auf einem clientseitigen **Recordset-Objekt**verwendet.

