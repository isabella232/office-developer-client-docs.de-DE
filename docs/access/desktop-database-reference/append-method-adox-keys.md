---
title: Append-Methode (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718903"
---
# <a name="append-method-adox-keys"></a>Append-Methode (ADOX Keys)

**Betrifft**: Access 2013, Office 2013

Fügt der [Keys](key-object-adox.md)-Auflistung ein neues [Key](keys-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Schlüssel*. Fügen Sie*Schlüssel* \[,*Schlüsseltyp* \] \[,*Spalte* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Key* |Das anzufügende **Key** -Objekt oder der Name des zu erstellenden und anzufügenden Schlüssels.|
|*Schlüsseltyp* |Optional. Ein **Long** -Wert, der den Schlüsseltyp angibt. Der Parameter *Schlüssel* entspricht der [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) -Eigenschaft eines **Key** -Objekts.|
|*Column* |Optional. Ein **String** -Wert, der den Namen der zu indizierenden Spalte angibt. Der *Columns* -Parameter entspricht dem Wert der [Name](name-property-adox.md) -Eigenschaft eines [Column](column-object-adox.md) -Objekts.|
|*RelatedTable* |Optional. Ein **String** -Wert, der den Namen der verknüpften Tabelle angibt. Der Parameter *RelatedTable* entspricht dem Wert der **Name** -Eigenschaft eines [Table](table-object-adox.md) -Objekts.|
|*RelatedColumn* |Optional. Ein String-Wert, der den Namen der verknüpften Spalte für einen Fremdschlüssel angibt. Der RelatedColumn-Parameter entspricht dem Wert der Name-Eigenschaft eines Column-Objekts.|

## <a name="remarks"></a>Hinweise

Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.

