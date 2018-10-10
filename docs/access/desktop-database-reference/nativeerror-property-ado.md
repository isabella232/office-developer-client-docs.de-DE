---
title: NativeError-Eigenschaft (ADO)
TOCTitle: NativeError Property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98d9695e29df63371b5ee375f864e7b1d4961ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476037"
---
# <a name="nativeerror-property-ado"></a>NativeError-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.

## <a name="remarks"></a>Hinweise

Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.

