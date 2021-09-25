---
title: Seek-Methode – ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bdf15631bc1897158e5efab5712434a5ef61eb07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580875"
---
# <a name="seek-method-ado"></a>Seek-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Durchsucht den Index eines [Recordset](recordset-object-ado.md)-Objekt, um auf schnelle Weise die Zeile zu finden, die den angegebenen Werten entspricht, und ändert die aktuelle Zeilenposition auf diese Zeile.

## <a name="syntax"></a>Syntax

*Recordset*. Seek *KeyValues*, *SeekOption*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*KeyValues* |Ein Array mit **Variant** -Werten. Ein Index besteht aus einer oder mehreren Spalten, und das Array enthält einen Wert, mit dem jede einzelne Spalte verglichen wird.|
|*SeekOption* |Ein [SeekEnum](seekenum.md)-Wert, der die Art des Vergleichs angibt, der zwischen den Spalten des Index und den entsprechenden *KeyValues* vorgenommen wird.|

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **Seek**-Methode in Verbindung mit der [Index](index-property-ado.md)-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset**-Objekt unterstützt. Mit der [Supports](supports-method-ado.md)**(adSeek)**-Methode bestimmen Sie, ob der zugrunde liegende Anbieter **Seek** unterstützt, und mit der **Supports(adIndex)**-Methode, ob der Anbieter Indizes unterstützt. (Beispielsweise werden **Seek** und **Index** vom [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt.)

Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.

This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.

Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit einem [CommandTypeEnum](commandtypeenum.md)-Wert für **adCmdTableDirect** geöffnet wurde.

