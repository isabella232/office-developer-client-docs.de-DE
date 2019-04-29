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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432317"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Konvertierungen zwischen MIME-Objekten und MAPI-Nachrichten. Dies kann beim Transportieren von Nachrichten über das Internet hilfreich sein.
  
|||
|:-----|:-----|
|Bereitgestellt von:  <br/> |CLSID_IConverterSession  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Gibt ein optionales MAPI-Adressbuch an, das vom MAPI-in-MIME-Konverter verwendet wird, um mehrdeutige Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream aufzulösen.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialisiert die Codierung, die während der Konvertierung verwendet werden soll.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Konvertiert einen MIME-Stream in eine MAPI-Nachricht.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Konvertiert eine MAPI-Nachricht in einen MIME-Stream.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Legt die Breite des Textumbruchs für einen MIME-Stream fest, der vom Konverter in **MAPIToMIMEStm**zurückgegeben wird.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Legt das Format fest, das der Konverter einen MIME-Stream in **MAPIToMIMEStm**zurückgibt.  <br/> |
| *Platzhalterelement*  <br/> | *Nicht unterstützt oder dokumentiert.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Gibt einen optionalen Zeichensatz an, den der MAPI-in-MIME-Konverter beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream verwendet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Aufrufen **** der setEncoding vor der Verwendung von **MAPIToMIMEStm** für die Konvertierung. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die MAPI-MIME-Konvertierungs-API](about-the-mapi-mime-conversion-api.md)
  
[MAPI-Konstanten](mapi-constants.md)

