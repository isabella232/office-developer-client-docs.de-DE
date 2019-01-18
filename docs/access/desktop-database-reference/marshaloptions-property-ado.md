---
title: MarshalOptions-Eigenschaft (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704595"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.

## <a name="remarks"></a>Hinweise

Wenn Sie ein clientseitiges [Recordset-Objekt](recordset-object-ado.md)verwenden, Datensätze, die auf dem Client geändert wurden zurückgeschrieben in der mittleren Ebene oder Webserver durch eine Technik Marshalling, das Packen und Senden der Parameter für die Benutzeroberfläche über Thread aufgerufen oder Grenzen zu verarbeiten. Festlegen der **MarshalOptions** -Eigenschaft kann die Leistung verbessern, wenn geänderte Remotedaten zum Aktualisieren der wieder auf der mittleren Ebene oder Webserver gemarshallt werden kann.

**Remote Data Service-Verwendung** Diese Eigenschaft wird nur auf einem clientseitigen **Recordset-Objekt**verwendet.

