---
title: Close-Methode (ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e36fb95ddb85312c1376948c819749e76e11945
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930966"
---
# <a name="close-method-ado-md"></a>Close-Methode (ADO MD)


**Betrifft**: Access 2013, Office 2013

Schließt eine geöffnete Zellmenge.

## <a name="syntax"></a>Syntax

*Zellmenge*. Schließen Sie

## <a name="remarks"></a>Hinweise

Durch das Verwenden der **Close** -Methode zum Schließen eines [Cellset](cellset-object-ado-md.md)-Objekts werden die verbundenen Daten freigegeben, einschließlich der Daten in allen verknüpften [Cell](cell-object-ado-md.md)-, [Axis](axis-object-ado-md.md)-, [Position](position-object-ado-md.md)- oder [Member](member-object-ado-md.md)-Objekten. Durch das Schließen eines **Cellset** -Objekts wird dieses nicht aus dem Speicher gelöscht. Sie können die Eigenschafteneinstellungen des Objekts ändern und es später erneut öffnen. Um ein Objekt vollständig aus dem Speicher zu entfernen, legen Sie die Objektvariable auf **Nothing** fest.

Sie können die [Open](open-method-ado-md.md)-Methode später aufrufen, um das **Cellset** -Objekt später mithilfe derselben oder einer anderen Quellzeichenfolge erneut zu öffnen. Während das **Cellset** -Objekt geschlossen ist, tritt ein Fehler auf, wenn Eigenschaften abgerufen oder Methoden aufgerufen werden, die auf die zugrunde liegenden Daten oder Metadaten verweisen.

