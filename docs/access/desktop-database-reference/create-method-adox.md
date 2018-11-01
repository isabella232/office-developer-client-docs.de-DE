---
title: Create-Methode (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91f5105611df85e007dea6d0e17e3104ea5987a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870254"
---
# <a name="create-method-adox"></a>Create-Methode (ADOX)


**Betrifft**: Access 2013, Office 2013


Erstellt einen neuen Katalog.

## <a name="syntax"></a>Syntax

*Katalog*. *ConnectString* erstellen

## <a name="parameters"></a>Parameters

  - *ConnectString*

  - Ein **String** -Wert, der verwendet wird, um eine Verbindung mit der Datenquelle herzustellen.

## <a name="remarks"></a>Hinweise

Die **Create**-Methode erstellt und öffnet ein neues ADO-[Connection](connection-object-ado.md)-Objekt für die in *ConnectString* angegebene Datenquelle. Bei erfolgreicher Ausführung wird das neue **Connection**-Objekt der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft zugewiesen.

Wenn der Anbieter das Erstellen von neuen Katalogen nicht unterstützt, tritt ein Fehler auf,.

