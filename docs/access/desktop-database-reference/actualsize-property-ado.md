---
title: ActualSize-Eigenschaft (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280432"
---
# <a name="actualsize-property-ado"></a>ActualSize-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt die tatsächliche Länge des Werts eines Felds an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Returns a **Long** value. Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.

## <a name="remarks"></a>Bemerkungen

Mithilfe der **ActualSize**-Eigenschaft geben Sie die tatsächliche Länge des Werts eines [Field](field-object-ado.md)-Objekts zurück. Die **ActualSize**-Eigenschaft ist für alle Felder schreibgeschützt. Falls ADO die Länge des Werts für das **Field**-Objekt nicht bestimmen kann, wird **adUnknown** von der **ActualSize**-Eigenschaft zurückgegeben.

Die Eigenschaften **ActualSize** und [DefinedSize](definedsize-property-ado.md) sind unterschiedlich. A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record. **Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.

