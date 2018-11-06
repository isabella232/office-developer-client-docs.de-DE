---
title: SetEOS-Methode (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b45e716844b3e616dfe5b8f94d69f29d6b0f1042
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997511"
---
# <a name="seteos-method-ado"></a>SetEOS-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. SetEOS

## <a name="remarks"></a>Hinweise

**SetEOS** aktualisiert den Wert der [EOS](eos-property-ado.md)-Eigenschaft, indem sie die aktuelle [Position](position-property-ado.md) als das Ende des Datenstroms festlegt. Alle nach der aktuellen Position folgenden Bytes oder Zeichen werden abgeschnitten.

Da [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) und [CopyTo](copyto-method-ado.md) keine zusätzlichen Werte in vorhandenen **Stream** -Objekten abschneiden, können Sie diese Bytes oder Zeichen abschneiden, indem Sie diese Position mithilfe von **SetEOS** als neues Ende des Datenstroms festlegen.

> [!WARNING]
> Wenn Sie **EOS** auf eine Position vor dem tatsächlichen Ende des Datenstroms festlegen, gehen alle Daten, die nach der neuen **EOS** -Position folgen, verloren.