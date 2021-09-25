---
title: Append-Methode (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ae56acce889c6931c30603c02869953b2141e210
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559010"
---
# <a name="append-method-adox-indexes"></a>Append-Methode (ADOX Indexes)


**Gilt für**: Access 2013, Office 2013



Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Indizes*. Append *Index* \[ ,*Columns*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.|
|*Columns* |Optional. Ein **Variant**-Wert, der den bzw. die Namen der zu indizierenden Spalte(n) angibt. Der *Columns*-Parameter entspricht dem Wert bzw. den Werten der [Name](name-property-adox.md)-Eigenschaft eines bzw. mehrerer [Column](column-object-adox.md)-Objekte.|

## <a name="remarks"></a>HinwBemerkungeneise

Der *Columns*-Parameter kann entweder den Namen einer Spalte oder einen Array von Spaltennamen festlegen.

Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.

