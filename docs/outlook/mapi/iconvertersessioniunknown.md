---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99415e9b3996ead409df7bd99379d39e9a62370e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567627"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Konvertierungen zwischen MIME-Objekten und MAPI-Nachrichten. Dies kann beim Übertragen von Nachrichten über das Internet hilfreich sein.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |CLSID_IConverterSession  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Gibt ein optionales MAPI-Adressbuch an, das vom MAPI-zu-MIME-Konverter verwendet wird, um mehrdeutige Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream aufzulösen.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialisiert die Codierung, die während der Konvertierung verwendet werden soll.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Konvertiert einen MIME-Datenstrom in eine MAPI-Nachricht.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Konvertiert eine MAPI-Nachricht in einen MIME-Stream.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Legt die Textumbruchbreite für einen MIME-Datenstrom fest, den der Konverter in **MAPIToMIMEStm** zurückgibt.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Legt das Format fest, das der Konverter einen MIME-Stream in **MAPIToMIMEStm** zurückgibt.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Gibt einen optionalen Zeichensatz an, den der MAPI-in-MIME-Konverter verwendet, wenn eine MAPI-Nachricht in einen MIME-Stream konvertiert wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie **"SetEncoding"** auf, bevor **Sie MAPIToMIMEStm** zum Ausführen der Konvertierung verwenden. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die MAPI-MIME-Konvertierungs-API](about-the-mapi-mime-conversion-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

