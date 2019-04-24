---
title: Append-Methode (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297095"
---
# <a name="append-method-adox-indexes"></a>Append-Methode (ADOX Indexes)


**Gilt für**: Access 2013, Office 2013



Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Indizes*. Anfügen von*Index* \[,*Spalten*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.|
|*Columns* |Optional. Ein **Variant**-Wert, der den bzw. die Namen der zu indizierenden Spalte(n) angibt. Der *Columns*-Parameter entspricht dem Wert bzw. den Werten der [Name](name-property-adox.md)-Eigenschaft eines bzw. mehrerer [Column](column-object-adox.md)-Objekte.|

## <a name="remarks"></a>Bemerkungen

Der *Columns*-Parameter kann entweder den Namen einer Spalte oder einen Array von Spaltennamen festlegen.

Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.

