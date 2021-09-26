---
title: Flush-Methode – ActiveX Data Objects (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d6305b2e4e33dea1ed36cd9bcc4b9a47ffae3a4d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622221"
---
# <a name="flush-method-ado"></a>Flush-Methode (ADO)


**Gilt für**: Access 2013, Office 2013

Erzwingt, dass der Inhalt des im ADO-Puffer verbleibenden [Stream](stream-object-ado.md)-Objekts an das zugrundeliegende Objekt, dem das **Stream**-Objekt zugeordnet ist, übergeben wird.

## <a name="syntax"></a>Syntax

*Stream*. Flush

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um den Inhalt des Datenstrompuffers an das zugrundeliegende Objekt (z. B. den Knoten oder die Datei, der bzw. die durch die URL dargestellt wird, bei der es sich um die Quelle des **Stream**-Objekts handelt). Diese Methode sollte aufgerufen werden, wenn Sie sicherstellen möchten, dass alle am Inhalt des **Stream**-Objekts vorgenommenen Änderungen geschrieben wurden. Bei ADO muss **Flush** in der Regel nicht aufgerufen werden, da ADO seinen Puffer in den meisten Fällen im Hintergrund leert. Die Änderungen am Inhalt eines **Stream**-Objekts werden automatisch vorgenommen und erst zwischengespeichert, wenn **Flush** aufgerufen wird.

Wenn Sie ein **Stream** -Objekt mit der [Close](close-method-ado.md)-Methode schließen, wird der Inhalt des **Stream** -Objekts automatisch geleert. Es ist nicht notwendig, **Flush** explizit unmittelbar vor **Close** aufzurufen.

