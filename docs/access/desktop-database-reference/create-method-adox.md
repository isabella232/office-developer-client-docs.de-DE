---
title: Create-Methode (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295422"
---
# <a name="create-method-adox"></a>Create-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Erstellt einen neuen Katalog.

## <a name="syntax"></a>Syntax

*Katalog*. Erstellen** von connectcollection

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectString* |Ein **String** -Wert, der verwendet wird, um eine Verbindung mit der Datenquelle herzustellen.|

## <a name="remarks"></a>Bemerkungen

Die **Create**-Methode erstellt und öffnet ein neues ADO-[Connection](connection-object-ado.md)-Objekt für die in *ConnectString* angegebene Datenquelle. Bei erfolgreicher Ausführung wird das neue **Connection**-Objekt der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft zugewiesen.

Wenn der Anbieter das Erstellen von neuen Katalogen nicht unterstützt, tritt ein Fehler auf,.

