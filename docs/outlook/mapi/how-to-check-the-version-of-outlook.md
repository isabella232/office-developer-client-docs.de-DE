---
title: Überprüfen Sie die Version von Outlook
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 672fc380-a29b-4e99-9211-949fd5065723
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 6369ea8948ae1996b6f88bcacd218b8dcf397306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574692"
---
# <a name="check-the-version-of-outlook"></a>Überprüfen Sie die Version von Outlook

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enth�lt ein Codebeispiel, in dem Informationen zur Version der installierten Versionen von Microsoft Outlook �berpr�ft, ob die installierte Version Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 oder Microsoft Outlook 2003 ist. �berpr�fen der Version der Outlook ist manchmal erforderlich sind, um sicherzustellen, dass bei einem MAPI-Anwendung Aufrufe API-Elemente, die durch die aktuell ausgef�hrte Version von Outlook unterst�tzt werden.

Im folgenden Codebeispiel  `PrintOutlookVersionString`, ruft Vollversion Zeichenfolgen mithilfe der **MsiProvideQualifiedComponent** und **MsiGetFileVersion** -Funktionen, wie in der Datei Msi.h im Microsoft Windows Software Development Kit (SDK) deklariert.  `PrintOutlookVersionString` gibt auch einen Zeiger auf eine Boolean-Variable, die angibt, ob eine 64-Bit-Version von Outlook installiert ist. Informationen zu den erwarteten Werten f�r die verschiedenen Teile einer Zeichenfolge Version f�r einige ver�ffentlichten Versionen von Outlook finden Sie unter [Gewusst wie: Bestimmen der Outlook-Versionsinformationen](http://support.microsoft.com/kb/870929).
  
```cpp
void PrintOutlookVersionString()
{
TCHAR pszOutlookQualifiedComponents[][MAX_PATH] = {
TEXT("{E83B4360-C208-4325-9504-0D23003A74A5}"), // Outlook 2013
TEXT("{1E77DE88-BCAB-4C37-B9E5-073AF52DFD7A}"), // Outlook 2010
TEXT("{24AAE126-0911-478F-A019-07B875EB9996}"), // Outlook 2007
TEXT("{BC174BAD-2F53-4855-A1D5-0D575C19B1EA}")  // Outlook 2003
};
int nOutlookQualifiedComponents = _countof(pszOutlookQualifiedComponents);
int i = 0;
UINT ret = 0;
for (i = 0; i < nOutlookQualifiedComponents; i++)
{
DWORD dwValueBuf = 0;
LPTSTR pszTempPath = NULL;
LPTSTR pszTempVer = NULL;
bool b64 = false;
ret = pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.x64.exe"),
(DWORD) INSTALLMODE_DEFAULT,
NULL,
&dwValueBuf);
if (ERROR_SUCCESS == ret)
{
b64 = true;
}
else
{
ret = pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.exe"),
(DWORD) INSTALLMODE_DEFAULT,
NULL,
&dwValueBuf);
if (ERROR_SUCCESS == ret)
{
b64 = false;
}
}
if (ret == ERROR_SUCCESS)
{
dwValueBuf += 1;
pszTempPath = (LPTSTR) malloc(dwValueBuf * sizeof(TCHAR));
if (pszTempPath != NULL)
{
if (ERROR_SUCCESS == pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.exe"),
(DWORD) INSTALLMODE_EXISTING,
pszTempPath,
&dwValueBuf))
{
pszTempVer = (LPTSTR) malloc(MAX_PATH * sizeof(TCHAR));
dwValueBuf = MAX_PATH;
if (ERROR_SUCCESS == pfnMsiGetFileVersion(pszTempPath,
pszTempVer,
&dwValueBuf,
NULL,
NULL))
{
printf("Path: %s\nVersion: %s\n64 bit: %s\n", pszTempPath, pszTempVer, b64?_T("true"):_T("false"));
}
}
}
free(pszTempVer);
free(pszTempPath);
}
}
}HRESULT GetOutlookVersionString(LPTSTR* ppszVer, BOOL* pf64Bit)
{
    HRESULT hr = E_FAIL;
    LPTSTR pszTempPath = NULL;
    LPTSTR pszTempVer = NULL;
    TCHAR pszOutlookQualifiedComponents[][MAX_PATH] = {
        TEXT("{E83B4360-C208-4325-9504-0D23003A74A5}"), // Outlook 2013
        TEXT("{1E77DE88-BCAB-4C37-B9E5-073AF52DFD7A}"), // Outlook 2010
        TEXT("{24AAE126-0911-478F-A019-07B875EB9996}"), // Outlook 2007
        TEXT("{BC174BAD-2F53-4855-A1D5-0D575C19B1EA}")  // Outlook 2003
    };
    int nOutlookQualifiedComponents = _countof(pszOutlookQualifiedComponents);
    int i = 0;
    DWORD dwValueBuf = 0;
    UINT ret = 0;
    *pf64Bit = FALSE;
    for (i = 0; i < nOutlookQualifiedComponents; i++)
    {
        ret = MsiProvideQualifiedComponent(
            pszOutlookQualifiedComponents[i],
            TEXT("outlook.x64.exe"),
            (DWORD) INSTALLMODE_DEFAULT,
            NULL,
            &dwValueBuf);
        if (ERROR_SUCCESS == ret) break;
    }
    if (ret != ERROR_SUCCESS)
    {
        for (i = 0; i < nOutlookQualifiedComponents; i++)
        {
            ret = MsiProvideQualifiedComponent(
                pszOutlookQualifiedComponents[i],
                TEXT("outlook.exe"),
                (DWORD) INSTALLMODE_DEFAULT,
                NULL,
                &dwValueBuf);
            if (ERROR_SUCCESS == ret) break;
        }
    }
    else
    {
        *pf64Bit = TRUE;
    }
    if (ret == ERROR_SUCCESS)
    {
        dwValueBuf += 1;
        pszTempPath = (LPTSTR) malloc(dwValueBuf * sizeof(TCHAR));
        if (pszTempPath != NULL)
        {
            if ((ret = MsiProvideQualifiedComponent(
                pszOutlookQualifiedComponents[i],
                TEXT("outlook.exe"),
                (DWORD) INSTALLMODE_EXISTING,
                pszTempPath,
                &dwValueBuf)) != ERROR_SUCCESS)
            {
                goto Error;
            }
            pszTempVer = (LPTSTR) malloc(MAX_PATH * sizeof(TCHAR));
            dwValueBuf = MAX_PATH;
            if ((ret = MsiGetFileVersion(pszTempPath,
                pszTempVer,
                &dwValueBuf,
                NULL,
                NULL))!= ERROR_SUCCESS)
            {
                goto Error;    
            }
            *ppszVer = pszTempVer;
            pszTempVer = NULL;
            hr = S_OK;
        }
    }
Error:
    free(pszTempVer);
    free(pszTempPath);
    return hr;
}

```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)

