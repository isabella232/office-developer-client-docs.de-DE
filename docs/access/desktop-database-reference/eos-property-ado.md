---
title: EOS-Eigenschaft (ADO - Access-desktop-Datenbank (engl.)))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716600"
---
# <a name="eos-property-ado"></a>EOS-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt an, ob sich die aktuelle Position am Ende des Datenstroms befindet.

## <a name="return-values"></a>Rückgabewerte

Gibt einen Wert vom Datentyp **Boolean** zurück, der angibt, ob sich die aktuelle Position am Ende des Datenstroms befindet. **EOS** gibt **True** zurück, wenn keine Bytes mehr im Datenstrom vorhanden sind. Wenn auf die aktuelle Position noch Bytes folgen, wird **False** zurückgegeben.

Verwenden Sie die [SetEOS](seteos-method-ado.md)-Methode, um das Ende der Datenstromposition festzulegen. Mithilfe der [Position](position-property-ado.md)-Eigenschaft bestimmen Sie die aktuelle Position.

