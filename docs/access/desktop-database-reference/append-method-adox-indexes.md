---
title: Append-Methode (ADOX Indexes)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473459"
---
# <a name="append-method-adox-indexes"></a>Append-Methode (ADOX Indexes)


**Betrifft**: Access 2013 | Office 2013



Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Indizes*. Fügen Sie*Index* \[,*Spalten*\]

## <a name="parameters"></a>Parameter

  - *Index*

  - Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.

  - *Columns*

  - Optional. Ein **Variant** -Wert, der die Namen der zu indizierenden Spalte(n) angibt. Die Werte der [Name](name-property-adox.md) -Eigenschaft des ein [Column](column-object-adox.md) -Objekt oder Objekte entspricht der *Columns* -Parameter.

## <a name="remarks"></a>Hinweise

Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.

Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.

