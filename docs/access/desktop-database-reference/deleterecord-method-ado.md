---
title: DeleteRecord-Methode (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472831"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013



Löscht eine durch [Record](record-object-ado.md) dargestellte Entität.

## <a name="syntax"></a>Syntax

*Datensatz*. **DeleteRecord *** Quelle*, *Async*

## <a name="parameters"></a>Parameter

  - *Source*

  - Optional. Ein String-Wert mit einer URL, die die zu löschende Entität (z. B. eine Datei oder ein Verzeichnis) identifiziert. Wenn Source nicht angeben ist oder eine leere Zeichenfolge angibt, wird die durch den aktuellen Record dargestellte Entität gelöscht. Wenn es sich bei Record um einen Datensatz einer Auflistung (RecordType von adCollectionRecord, z. B. einem Verzeichnis) handelt, werden alle untergeordneten Ebenen (z. B. Unterverzeichnisse) ebenso gelöscht.

  - *Async*

  - Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass der Löschvorgang asynchron ist.

## <a name="remarks"></a>Hinweise

Vorgänge in Bezug auf das durch diesen **Record** dargestellte Objekt schlagen möglicherweise fehl, nachdem das Ausführen dieser Methode beendet wurde. Nach dem Aufrufen von **DeleteRecord** sollte **Record** geschlossen werden, da das Verhalten von **Record** in Abhängigkeit davon, wann der Anbieter den **Record** mit der Datenquelle aktualisiert, möglicherweise unvorhersehbar wird.

Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, werden die Ergebnisse dieses Vorgangs nicht unmittelbar im **Recordset** -Objekt wiedergegeben. Aktualisieren Sie das **Recordset** , indem schließen und erneut öffnen, oder durch Ausführen der **Recordset** [erneut abzufragen](requery-method-ado.md), oder [Update](update-method-ado.md) und [Resync](resync-method-ado.md) -Methode.


> [!NOTE]
> <P>[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider für Internet Publishing</A> automatisch aufgerufen. Weitere Informationen erhalten Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</P>


