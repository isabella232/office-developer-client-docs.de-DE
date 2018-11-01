---
title: Flush-Methode - ActiveX Data Objects (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ecf56ccf715df324798cd9b5adfc57f92591f05
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885129"
---
# <a name="flush-method-ado"></a>Flush-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Erzwingt, dass der Inhalt des im ADO-Puffer verbleibenden [Stream](stream-object-ado.md)-Objekts an das zugrundeliegende Objekt, dem das **Stream** -Objekt zugeordnet ist, übergeben wird.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. Leeren

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um den Inhalt des Datenstrompuffers an das zugrundeliegende Objekt (z. B. den Knoten oder die Datei, der bzw. die durch die URL dargestellt wird, bei der es sich um die Quelle des **Stream** -Objekts handelt). Diese Methode sollte aufgerufen werden, wenn Sie sicherstellen möchten, dass alle am Inhalt des **Stream** -Objekts vorgenommenen Änderungen geschrieben wurden. Bei ADO muss **Flush** in der Regel nicht aufgerufen werden, da ADO seinen Puffer in den meisten Fällen im Hintergrund leert. Die Änderungen am Inhalt eines **Stream** -Objekts werden automatisch vorgenommen und erst zwischengespeichert, wenn **Flush** aufgerufen wird.

Wenn Sie ein **Stream** -Objekt mit der [Close](close-method-ado.md)-Methode schließen, wird der Inhalt des **Stream** -Objekts automatisch geleert. Es ist nicht notwendig, **Flush** explizit unmittelbar vor **Close** aufzurufen.

