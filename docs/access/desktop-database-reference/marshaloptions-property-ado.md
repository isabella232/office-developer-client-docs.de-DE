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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289770"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.

## <a name="remarks"></a>Bemerkungen

Bei Verwendung eines clientseitigen [Recordset-Objekts](recordset-object-ado.md)werden Datensätze, die auf dem Client geändert wurden, über eine Technik namens "Marshalling" zurück auf die mittlere Ebene oder den Webserver geschrieben, der Prozess des Packens und Sendens von Schnittstellenmethoden Parametern über den Thread oder Prozessgrenzen. Das Festlegen **** der MarshalOptions-Eigenschaft kann die Leistung verbessern, wenn geänderte Remotedaten für die Aktualisierung zurück auf die mittlere Ebene oder den Webserver gemarshallt werden.

**Remote Data Service-Verwendung** Diese Eigenschaft wird nur für ein clientseitiges **Recordset**-Objekt verwendet.

