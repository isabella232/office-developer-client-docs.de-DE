---
title: Append-Methode (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d296aed4b0ae64c5d165eeac89eed50859ee0c01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607346"
---
# <a name="append-method-adox-keys"></a>Append-Methode (ADOX Keys)

**Gilt für**: Access 2013, Office 2013

Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Keys*. Append *Key* \[ ,*KeyType* \] \[ ,*Column* \] \[ ,*RelatedTable* \] \[ ,*RelatedColumn*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Key* |Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.|
|*Keytype* |Optional. Ein **Long**-Wert, der den Schlüsseltyp angibt. Der *Key*-Parameter entspricht der [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)-Eigenschaft eines **Key**-Objekts.|
|*Spalte* |Optional. Ein **String**-Wert, der den Namen der zu indizierenden Spalte angibt. Der *Columns*-Parameter entspricht dem Wert der [Name](name-property-adox.md)-Eigenschaft eines [Column](column-object-adox.md)-Objekts.|
|*Relatedtable* |Optional. Ein **String**-Wert, der den Namen der verknüpften Tabelle angibt. Der *RelatedTable*-Parameter entspricht dem Wert der **Name**-Eigenschaft eines [Table](table-object-adox.md)-Objekts.|
|*RelatedColumn* |Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.|

## <a name="remarks"></a>HinwBemerkungeneise

Der *Columns*-Parameter kann entweder den Namen einer Spalte oder einen Array von Spaltennamen festlegen.

