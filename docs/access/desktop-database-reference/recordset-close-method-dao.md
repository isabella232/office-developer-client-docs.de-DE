---
title: Recordset.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2cde1f91affb1a50d050feaa1fb5d637ab2e9b43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597030"
---
# <a name="recordsetclose-method-dao"></a>Recordset.Close-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Schließt ein geöffnetes **Recordset**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* .Close

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Recordset**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Wenn Sie versuchen, ein **Connection**-Objekt zu schließen, für das noch **Recordset**-Objekte geöffnet sind, werden die **Recordset**-Objekte geschlossen, und alle ausstehenden Aktualisierungen oder Bearbeitungen werden abgebrochen. Auch wenn Sie versuchen, ein **Workspace**-Objekt zu schließen, für das noch **Connection**-Objekte geöffnet sind, werden diese **Connection**-Objekte geschlossen. Daraufhin werden deren **Recordset**-Objekte ebenfalls geschlossen.

Eine Alternative zur **Close**-Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).

