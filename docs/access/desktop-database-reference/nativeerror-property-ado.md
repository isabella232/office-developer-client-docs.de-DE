---
title: NativeError-Eigenschaft (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705946"
---
# <a name="nativeerror-property-ado"></a>NativeError-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.

## <a name="remarks"></a>Hinweise

Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.

