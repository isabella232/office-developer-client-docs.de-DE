---
title: DateModified-Eigenschaft (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472980"
---
# <a name="datemodified-property-adox"></a>DateModified-Eigenschaft (ADOX)


**Betrifft**: Access 2013 | Office 2013

Gibt das Datum an, an dem das Objekt zuletzt geändert wurde.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaft gibt einen **Variant** -Wert zurück, der das Änderungsdatum angibt. Der Wert ist Null, wenn **DateModified** nicht vom Anbieter unterstützt wird.

## <a name="remarks"></a>Hinweise

Die **DateModified** -Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateModified** -Eigenschaft abzurufen.

