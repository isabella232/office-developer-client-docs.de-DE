---
title: Dynamische Recordset-Eigenschaften in XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6b61504b6c88b1ccf2a7ff91756e821ae7a2f7af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617657"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Dynamische Recordset-Eigenschaften in XML

**Gilt für**: Access 2013, Office 2013

Die folgenden anbieterspezifischen Eigenschaften des **Recordset** -Objekts (im Client Cursor Engine) werden derzeit im XML-Format gespeichert:

- **AutoRecalc**
- **BatchSize**
- **Commandtimeout**
- **Irowsetchange**
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
