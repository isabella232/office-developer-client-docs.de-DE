---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e6880a32e30b8f208ce5ba0a2d30e635ff464461
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792033"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="192de-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="192de-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="192de-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="192de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="192de-105">Gibt ein optionales MAPI-Adressbuch, die MAPI zu MIME-Konverter verwendet, um mehrdeutige Adressen aufzulösen, beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="192de-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="192de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="192de-106">Parameters</span></span>

 <span data-ttu-id="192de-107">_PAB_</span><span class="sxs-lookup"><span data-stu-id="192de-107">_pab_</span></span>
  
> <span data-ttu-id="192de-108">[in] Zeiger auf eine [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) Schnittstelle in der MAPI in MIME-Konvertierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="192de-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="192de-109">Legen Sie diesen Parameter auf **null festgelegt** , wenn Sie nicht mehr im Adressbuch benötigen; Dies gibt die Schnittstelle und setzt den Konverter auf beliebiges Adressbuch nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="192de-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="192de-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="192de-110">Return value</span></span>

<span data-ttu-id="192de-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="192de-111">S_OK</span></span>
  
> <span data-ttu-id="192de-112">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="192de-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="192de-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="192de-113">Remarks</span></span>

<span data-ttu-id="192de-114">Konvertieren von MAPI erforderlich keine Nachrichten in MIME-Stream-Objekt im Allgemeinen Protokollierung bei einem MAPI-Profil.</span><span class="sxs-lookup"><span data-stu-id="192de-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="192de-115">Angeben von einem MAPI-Adressbuch für die Konvertierung erfordert jedoch zu einem Profil Abrufen des Adressbuchs anmelden.</span><span class="sxs-lookup"><span data-stu-id="192de-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="192de-116">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="192de-116">MFCMAPI reference</span></span>

<span data-ttu-id="192de-117">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="192de-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="192de-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="192de-118">**File**</span></span>|<span data-ttu-id="192de-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="192de-119">**Function**</span></span>|<span data-ttu-id="192de-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="192de-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="192de-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="192de-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="192de-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="192de-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="192de-123">MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="192de-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="192de-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="192de-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="192de-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="192de-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="192de-126">MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="192de-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="192de-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="192de-127">See also</span></span>



[<span data-ttu-id="192de-128">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="192de-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="192de-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="192de-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="192de-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="192de-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="192de-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="192de-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="192de-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="192de-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="192de-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="192de-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="192de-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="192de-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

