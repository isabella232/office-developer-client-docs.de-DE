---
title: Seek-Methode - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726302"
---
# <a name="seek-method-ado"></a>Seek-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Durchsucht den Index eines [Recordset](recordset-object-ado.md)-Objekt, um auf schnelle Weise die Zeile zu finden, die den angegebenen Werten entspricht, und ändert die aktuelle Zeilenposition auf diese Zeile.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. Seek*KeyValues entspricht*, *SeekOption*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*KeyValues* |Ein Array mit **Variant** -Werten. Ein Index besteht aus einer oder mehreren Spalten, und das Array enthält einen Wert, mit dem jede einzelne Spalte verglichen wird.|
|*SeekOption* |Ein [SeekEnum](seekenum.md)-Wert, der die Art des Vergleichs angibt, der zwischen den Spalten des Index und den entsprechenden *KeyValues* vorgenommen wird.|

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Seek** -Methode in Verbindung mit der [Index](index-property-ado.md)-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset** -Objekt unterstützt. Verwenden Sie die Methode, um zu bestimmen, ob der zugrunde liegenden Anbieter **Seek**unterstützt [unterstützt](supports-method-ado.md)**(AdSeek)** und die **Supports(adIndex)** -Methode, um festzustellen, ob der Anbieter Indizes unterstützt. (Beispielsweise werden [Seek](microsoft-ole-db-provider-for-microsoft-jet.md) und **Index** vom **OLE DB-Anbieter für Microsoft Jet** unterstützt.)

Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.

Diese Methode wird nur bei serverseitigen Cursors unterstützt. Seek wird nicht unterstützt, wenn der Wert der CursorLocation-Eigenschaft des Recordset-Objekts adUseClient lautet.

Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit einem [CommandTypeEnum](commandtypeenum.md)-Wert für **adCmdTableDirect** geöffnet wurde.

