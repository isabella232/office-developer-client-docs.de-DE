---
title: Delete-Methode (ADOX-Auflistungen)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294078"
---
# <a name="delete-method-adox-collections"></a>Delete-Methode (ADOX-Auflistungen)

**Gilt für**: Access 2013, Office 2013

Entfernt ein Objekt aus einer Auflistung.

## <a name="syntax"></a>Syntax

*Sammlung*. *Name* löschen

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Ein **Variant** -Wert, der den Namen oder die Position (Index) des zu löschenden Objekts angibt.|

## <a name="remarks"></a>Bemerkungen

Wenn der Name nicht in der Auflistung vorhanden ist, tritt ein Fehler auf.

Für [Tables](tables-collection-adox.md)- und [Users](users-collection-adox.md)-Auflistungen tritt ein Fehler auf, wenn der Anbieter das Löschen von Tabellen oder gegebenenfalls Benutzern nicht unterstützt. Für [Procedures](procedures-collection-adox.md)- und [Views](views-collection-adox.md)-Auflistungen tritt bei der Verwendung von **Delete** ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.

