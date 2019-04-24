---
title: Dynamische Recordset-Eigenschaften in XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307658"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Dynamische Recordset-Eigenschaften in XML

**Gilt für**: Access 2013, Office 2013

Die folgenden anbieterspezifischen Eigenschaften des **Recordset** -Objekts (im Client Cursor Engine) werden derzeit im XML-Format gespeichert:

- **AutoRecalc**
- **BatchSize**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Reshape Name**
- **Resync Command**
- **Unique Catalog**
- **Unique Schema**
- **Unique Table**
- **Update Resync**
- **UpdateCriteria**


Diese Eigenschaften werden im Schemaabschnitt als Attribute der Elementdefinition für das **Recordset** -Objekt gespeichert. Diese Attribute werden im Rowsetschemanamespace definiert und müssen das Präfix "rs:" enthalten.

## <a name="see-also"></a>Siehe auch

- [Dynamische ADO-Eigenschaften](ado-dynamic-properties.md)
