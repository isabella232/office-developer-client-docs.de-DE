---
title: Delete-Methode (ADOX Collections)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5fdcd80a49d7d9d14ba17a85f675fdfd9906c1b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921663"
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

