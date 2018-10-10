---
title: Create-Methode (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475457"
---
# <a name="create-method-adox"></a>Create-Methode (ADOX)


**Betrifft**: Access 2013 | Office 2013


Erstellt einen neuen Katalog.

## <a name="syntax"></a>Syntax

*Katalog*. *ConnectString* erstellen

## <a name="parameters"></a>Parameters

  - *ConnectString*

  - Ein **String** -Wert, der verwendet wird, um eine Verbindung mit der Datenquelle herzustellen.

## <a name="remarks"></a>Hinweise

Die **Create**-Methode erstellt und öffnet ein neues ADO-[Connection](connection-object-ado.md)-Objekt für die in *ConnectString* angegebene Datenquelle. Bei erfolgreicher Ausführung wird das neue **Connection**-Objekt der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft zugewiesen.

Wenn der Anbieter das Erstellen von neuen Katalogen nicht unterstützt, tritt ein Fehler auf,.

