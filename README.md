## taken from:
[spacemacs evilify](https://github.com/syl20bnr/spacemacs/blob/b7e51d70aa3fb81df2da6dc16d9652a002ba5e6b/layers/%2Bdistributions/spacemacs-base/local/evil-evilified-state/evil-evilified-state.el)

## to install
```
     (use-package evil-evilified-state
       :load-path "path/where/you/cloned/evil-evilified-state")
```

## example
```
     (use-package dired
       :defer t
       :config
       (evilified-state-evilify dired-mode dired-mode-map
                                "j"         'evil-next-line
                                "k"         'evil-previous-line
                                "-"         'dired-up-directory
                                "0"         'dired-back-to-start-of-files
                                (kbd "C-j") 'dired-next-subdir
                                (kbd "C-k") 'dired-prev-subdir
                                "I"         'vinegar/dotfiles-toggle
                                (kbd "~")   '(lambda ()(interactive) (find-alternate-file "~/"))
                                (kbd "RET") 'dired-find-file-other-window
                                "f"         'helm-find-files
                                "J"         'dired-goto-file
                                (kbd "C-f") 'find-name-dired
                                "H"         'diredp-dired-recent-dirs
                                "T"         'dired-tree-down
                                "K"         'dired-do-kill-lines
                                "r"         'revert-buffer
                                (kbd "C-r") 'dired-do-redisplay
                                "gg"        'evil-goto-first-line
                                "G"         'evil-goto-line))

```
