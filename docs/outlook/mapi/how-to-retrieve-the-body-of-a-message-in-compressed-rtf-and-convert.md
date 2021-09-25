---
title: Abrufen des Nachrichtentexts in komprimierter RTF und Konvertieren in das systemeigene Format
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9408da71-4abf-60cf-5412-58c5ceeb2205
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 30879323c81f51e80c8e1f66da5c1b424a882c98
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564267"
---
# <a name="retrieve-body-of-message-in-compressed-rtf-and-convert-to-its-native-format"></a>Abrufen des Nachrichtentexts in komprimierter RTF und Konvertieren in das systemeigene Format

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Codebeispiel in Microsoft C++ wird gezeigt, wie Sie die exportierte Microsoft Outlook 2010 oder Microsoft Outlook 2013-Funktion [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) verwenden, um auf den Text einer Nachricht zuzugreifen, die in komprimierter RTF gekapselt ist, und um den Textkörper im systemeigenen Format abzurufen. 
  
```cpp
//These are definitions for the WrapCompressedRTFStreamEx function. 
typedef HRESULT (STDMETHODCALLTYPE WRAPCOMPRESSEDRTFSTREAMEX) ( 
    LPSTREAM lpCompressedRTFStream, CONST RTF_WCSINFO * pWCSInfo, LPSTREAM * lppUncompressedRTFStream, RTF_WCSRETINFO * pRetInfo); 
typedef WRAPCOMPRESSEDRTFSTREAMEX *LPWRAPCOMPRESSEDRTFSTREAMEX; 
 
HRESULT TestWrapCompressedRTFStreamEx(LPMESSAGE lpMsg) 
{ 
    HRESULT         hRes = S_OK; 
    LPSTREAM        lpCompressed = NULL; 
    LPSTREAM        lpUncompressed = NULL; 
    char            szBody[1024] = {0}; 
    ULONG           ulRead = 0; 
    RTF_WCSINFO     wcsinfo = {0}; 
    RTF_WCSRETINFO  retinfo = {0}; 
    LPSPropValue    lpPropCPID = NULL; 
 
    retinfo.size = sizeof(RTF_WCSRETINFO); 
 
    wcsinfo.size = sizeof(RTF_WCSINFO); 
    wcsinfo.ulFlags = MAPI_NATIVE_BODY; 
    wcsinfo.ulOutCodePage = 0; 
 
    // Retrieve the value of the Internet code page. 
    // Pass this value to the WrapCompressedRTFStreamEx function. 
    // If the property is not found, the default is 0. 
    if(SUCCEEDED(hRes = HrGetOneProp(lpMsg, PR_INTERNET_CPID, &lpPropCPID))) 
    { 
        wcsinfo.ulInCodePage = lpPropCPID->Value.l; 
    } 
 
    // Open the compressed RTF stream. 
    if(SUCCEEDED(hRes = lpMsg->OpenProperty(PR_RTF_COMPRESSED, 
                                         &IID_IStream, 
                                         STGM_READ | STGM_DIRECT, 
                                         0, 
                                         (LPUNKNOWN*)&lpCompressed))) 
    { 
 
        // Notice that the WrapCompressedRTFStreamEx function has been loaded 
        // by using the GetProcAddress function into pfnWrapEx. 
 
        // Call the WrapCompressedRTFStreamEx function. 
        if(SUCCEEDED(hRes = pfnWrapEx(lpCompressed, 
                                   &wcsinfo, 
                                   &lpUncompressed, 
                                   &retinfo))) 
        { 
 
            printf("Body's native type is: "); 
 
            // Check what the native body type is. 
            switch(retinfo.ulStreamFlags) 
            { 
            case MAPI_NATIVE_BODY_TYPE_RTF: 
                printf("MAPI_NATIVE_BODY_TYPE_RTF\n"); 
                break; 
            case MAPI_NATIVE_BODY_TYPE_HTML: 
                printf("MAPI_NATIVE_BODY_TYPE_HTML\n"); 
                break; 
            case MAPI_NATIVE_BODY_TYPE_PLAINTEXT: 
                printf("MAPI_NATIVE_BODY_TYPE_PLAINTEXT\n"); 
                break; 
            default: 
                printf("UNKNOWN\n"); 
            } 
 
            // Read the first 1,000 characters out of the stream. 
            if(SUCCEEDED(hRes = lpUncompressed->Read(szBody, 1024, &ulRead))) 
            { 
                printf("First %d characters of the native body stream:\n%s\n", ulRead, szBody); 
            } 
        } 
    } 
 
    MAPIFreeBuffer(lpPropCPID); 
    if(lpUncompressed)lpUncompressed->Release(); 
    if(lpCompressed)lpCompressed->Release(); 
 
    return hRes; 
} 

```


