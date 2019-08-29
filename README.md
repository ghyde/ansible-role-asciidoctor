# asciidoctor

Install [asciidoctor][asciidoctor] on Fedora.

## Role Variables

### defaults/main.yml

| name                            | description                                                      | type   | default |
| ------------------------------- | ---------------------------------------------------------------- | ------ | ------- |
| asciidoctor_install_pdf_package | Install [asciidoctor-pdf][pdf]                                   | Bool   | True    |
| asciidoctor_syntax_highlighter  | Syntax highlighter package, one of [rouge, pygments.rb, coderay] | String | rouge   |

### vars/main.yml

| name                           | description                               | type | default                       |
| ------------------------------ | ----------------------------------------- | ---- | ----------------------------- |
| asciidoctor_valid_highlighters | List of valid syntax highlighter packages | List | [rouge, pygments.rb, coderay] |

## Example Playbook

```yaml
- hosts: workstations
  tasks:
  - import_role:
      name: asciidoctor
    vars:
      asciidoctor_install_pdf_package: True
      asciidoctor_syntax_highlighter: rouge
```

## License

[MIT](LICENSE)

[asciidoctor]: https://asciidoctor.org
[pdf]: https://asciidoctor.org/docs/asciidoctor-pdf/
