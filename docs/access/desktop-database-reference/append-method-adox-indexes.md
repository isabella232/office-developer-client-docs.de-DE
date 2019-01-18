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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707556"
---
# <a name="append-method-adox-indexes"></a>Append-Methode (ADOX Indexes)


**Betrifft**: Access 2013, Office 2013



Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Indizes*. Fügen Sie*Index* \[,*Spalten*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Index* |Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.|
|*Columns* |Optional. Ein **Variant** -Wert, der die Namen der zu indizierenden Spalte(n) angibt. Die Werte der [Name](name-property-adox.md) -Eigenschaft des ein [Column](column-object-adox.md) -Objekt oder Objekte entspricht der *Columns* -Parameter.|

## <a name="remarks"></a>Bemerkungen

Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.

Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.

