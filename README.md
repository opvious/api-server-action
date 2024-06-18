# Set up API server action

```yaml
steps:
  # ...
  - name: Set up API server
    uses: opvious/api-server-action@main
    with:
      license-key: ${{ secrets.OPVIOUS_LICENSE_KEY }} # Optional
```


## Inputs

All inputs are optional.

+ `license-key`: license key to unlock advanced API capabilities
+ `image-tag`: [server image][] tag, defaults to `latest`
+ `log-level`: log level, defaults to `info`
+ `skip-node-setup`: skip Node setup action, useful if already done


## Outputs

This action has no outputs. It sets the `OPVIOUS_ENDPOINT` and `OPVIOUS_TOKEN`
environment variables appropriately for later use by SDKs. The [`opvious`
CLI][cli] is also installed for use in follow up steps.


## License

This action is licensed under Apache 2.0. The underlying [server image][] is
subject to the [Opvious API image EULA][eula].


[server image]: https://hub.docker.com/r/opvious/api-server
[eula]: https://www.opvious.io/end-user-license-agreements/api-image
[cli]: https://www.npmjs.com/package/opvious-cli
