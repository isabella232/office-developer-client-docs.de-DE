---
title: Create-Methode (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cf9d2b74aae4c13bb3e1349ffd4a7d23ed95b3aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626953"
---
# <a name="create-method-adox"></a>Create-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Erstellt einen neuen Katalog.

## <a name="syntax"></a>Syntax

*Catalog*. ConnectString *erstellen*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectString* |Ein **String** -Wert, der verwendet wird, um eine Verbindung mit der Datenquelle herzustellen.|

## <a name="remarks"></a>Bemerkungen

Die **Create**-Methode erstellt und öffnet ein neues ADO-[Connection](connection-object-ado.md)-Objekt für die in *ConnectString* angegebene Datenquelle. Bei erfolgreicher Ausführung wird das neue **Connection**-Objekt der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft zugewiesen.

Wenn der Anbieter das Erstellen von neuen Katalogen nicht unterstützt, tritt ein Fehler auf,.

