---
title: SetEOS-Methode (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 456bbf7c7235d0db01b29372ee8f70c364263cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472635"
---
# <a name="seteos-method-ado"></a>SetEOS-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013

Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. SetEOS

## <a name="remarks"></a>Hinweise

**SetEOS** aktualisiert den Wert der [EOS](eos-property-ado.md)-Eigenschaft, indem sie die aktuelle [Position](position-property-ado.md) als das Ende des Datenstroms festlegt. Alle nach der aktuellen Position folgenden Bytes oder Zeichen werden abgeschnitten.

Da [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) und [CopyTo](copyto-method-ado.md) keine zusätzlichen Werte in vorhandenen **Stream** -Objekten abschneiden, können Sie diese Bytes oder Zeichen abschneiden, indem Sie diese Position mithilfe von **SetEOS** als neues Ende des Datenstroms festlegen.


> [!WARNING]
> <P>Wenn Sie <STRONG>EOS</STRONG> auf eine Position vor dem tatsächlichen Ende des Datenstroms festlegen, gehen alle Daten, die nach der neuen <STRONG>EOS</STRONG> -Position folgen, verloren.</P>


