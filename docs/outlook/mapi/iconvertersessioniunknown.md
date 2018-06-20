---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792049"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession: IUnknown

  
  
**Betrifft**: Outlook 
  
Ermöglicht die Konvertierung zwischen MIME-Objekten und MAPI-Nachrichten. Dies kann insbesondere für die Übermittlung von Nachrichten über das Internet sein.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |CLSID_IConverterSession  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Gibt ein optionales MAPI-Adressbuch, die MAPI zu MIME-Konverter verwendet, um mehrdeutige Adressen aufzulösen, beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialisiert die während der Konvertierung zu verwendende Codierung.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Konvertiert einen MIME-Datenstrom an einem MAPI-Nachricht.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Konvertiert eine MAPI-Nachricht in einen MIME-Stream.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Legt den Textfluss Breite für einen MIME-Stream, den der Konverter in **MAPIToMIMEStm**zurückgibt.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Legt das Format an, dass der Konverter einen MIME-Stream in **MAPIToMIMEStm**zurückgegeben.  <br/> |
| *Platzhalter-member*  <br/> | *Nicht unterstützte oder dokumentiert.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Gibt an, dass ein optionales Zeichen festgelegt, dass die MAPI zu MIME-Konverter, beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Rufen Sie **SetEncoding** vor der Nutzung **MAPIToMIMEStm** Konvertierung ausführen. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Konvertierung MAPI-MIME-API](about-the-mapi-mime-conversion-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

