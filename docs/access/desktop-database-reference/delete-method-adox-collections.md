---
title: Delete-Methode (ADOX Collections)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a429c18890125f1c047c6356d250713ea5ea817
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944900"
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

