---
title: LoadFromFile-Methode (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63b8c2541714f432e92d310ce70ebe308db51685
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612036"
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Lädt den Inhalt einer vorhandenen Datei in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream*. LoadFromFile *FileName*

## <a name="parameters"></a>Parameter

|Name |Beschreibung|
|:----|:----------|
|*FileName* |Ein **String**-Wert, der den Namen der in das **Stream**-Objekt zu ladenden Datei enthält. *FileName* kann einen beliebigen gültigen Pfad und Namen im UNC-Format enthalten. Wenn die angegebene Datei nicht vorhanden ist, tritt ein Laufzeitfehler auf.|

## <a name="remarks"></a>HinwBemerkungeneise

Diese Methode kann verwendet werden, um den Inhalt einer lokalen Datei in ein **Stream**-Objekt zu laden (z. B. zum Hochladen des Inhalts einer lokalen Datei auf einen Server).

Das **Stream** -Objekt muss vor dem Aufrufen von **LoadFromFile** bereits geöffnet sein. Diese Methode ändert die Bindung des **Stream** -Objekts nicht. Es bleibt an das Objekt gebunden, das durch die URL oder den **Record** angegeben wird, mit der bzw. dem das **Stream** -Objekt ursprünglich geöffnet wurde.

**LoadFromFile** überschreibt den aktuellen Inhalt des **Stream** -Objekts mit den aus der Datei gelesenen Daten. Alle im **Stream** -Objekt vorhandenen Bytes werden mit dem Inhalt der Datei überschrieben. Alle zuvor vorhandenen und verbleibenden Bytes, die auf das von [LoadFromFile](eos-property-ado.md) erstellte **EOS** folgen, werden abgeschnitten.

Nach einem Aufruf von **LoadFromFile** wird die aktuelle Position auf den Anfang des **Datenstroms** festgelegt ([Position](position-property-ado.md) ist 0).

Da dem Anfang des Datenstroms zur Verschlüsselung zwei Bytes hinzugefügt werden können, entspricht die Größe des Datenstroms möglicherweise nicht genau der Größe der Datei, aus der dieser geladen wurde.

