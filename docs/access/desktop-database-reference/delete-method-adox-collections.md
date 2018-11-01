---
title: Delete-Methode (ADOX Collections)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bfb9e12f32da56aecd9338e51d6e4656714b6c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871332"
---
# <a name="delete-method-adox-collections"></a>Delete-Methode (ADOX Collections)


**Betrifft**: Access 2013, Office 2013



Entfernt ein Objekt aus einer Auflistung.

## <a name="syntax"></a>Syntax

*Auflistung*. Löschen von*Namen*

## <a name="parameters"></a>Parameter

  - *Name*

  - Ein **Variant** -Wert, der den Namen oder die Position (Index) des zu löschenden Objekts angibt.

## <a name="remarks"></a>Hinweise

Wenn der *Name* nicht in der Auflistung vorhanden ist, wird ein Fehler verursacht.

Für [Tables](tables-collection-adox.md)- und [Users](users-collection-adox.md)-Auflistungen tritt ein Fehler auf, wenn der Anbieter das Löschen von Tabellen oder gegebenenfalls Benutzern nicht unterstützt. Für [Procedures](procedures-collection-adox.md)- und [Views](views-collection-adox.md)-Auflistungen tritt bei der Verwendung von **Delete** ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.

