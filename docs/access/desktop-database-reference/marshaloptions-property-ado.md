---
title: MarshalOptions-Eigenschaft (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8fff5f725df8c53e3990ed1aacd519a0bfdf6f4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593999"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.

## <a name="remarks"></a>HinwBemerkungeneise

Bei Verwendung eines clientseitigen [Recordset-Objekts](recordset-object-ado.md)werden Datensätze, die auf dem Client geändert wurden, über eine als Marshaling bezeichnete Technik, das Packen und Senden von Schnittstellenmethodenparametern über Thread- oder Prozessgrenzen hinweg, auf die mittlere Ebene oder den Webserver zurückgeschrieben. Das Festlegen der **MarshalOptions-Eigenschaft** kann die Leistung verbessern, wenn geänderte Remotedaten für die Zurückaktualisierung auf die mittlere Ebene oder den Webserver gemarshallt werden.

**Remote data service usage** Diese Eigenschaft wird nur für ein clientseitiges **Recordset -Objekt** verwendet.

