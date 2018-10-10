---
title: URL-Eigenschaft (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472621"
---
# <a name="url-property-rds"></a>URL-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013



Gibt eine Zeichenfolge an, die eine relative oder absolute URL enthält.

Sie können die **URL** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [DataControl](datacontrol-object-rds.md)-Objekts oder zur Laufzeit in Skriptcode festlegen.

## <a name="syntax"></a>Syntax

Entwurfszeit: \<PARAM NAME = Wert "URL" = "Server"\>

Laufzeit: DataControl.URL="Server"

## <a name="parameters"></a>Parameter

  - *Server*

  - Ein **String** -Wert, der eine gültige URL enthält.

  - *DataControl*

  - Eine Objektvariable, die ein **DataControl** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

In der Regel identifiziert die URL eine ASP-Datei (Active Server Page), die ein [Recordset](recordset-object-ado.md)-Objekt erstellen und zurückgeben kann. Dadurch erhält der Benutzer ein **Recordset** -Objekt, ohne dass er das serverbasierte [DataFactory](datafactory-object-rdsserver.md)-Objekt aufrufen oder ein benutzerdefiniertes Geschäftsobjekt programmieren muss.

Wenn die **URL** -Eigenschaft festgelegt wurde, sendet die [SubmitChanges](submitchanges-method-rds.md)-Methode Änderungen an den Speicherort, der durch die URL angegeben wird.

